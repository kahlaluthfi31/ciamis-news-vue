# Ciamis News

Website portal berita seputar Kabupaten Ciamis, dengan panel admin untuk mengelola konten berita (CRUD). Dibuat sebagai proyek portofolio dengan kompleksitas tingkat menengah.
# Owner + Developer : Kahla Luthfiyah Halim
# Date : 12.33 04/09/2026

## Ringkasan

Ciamis News adalah platform berita lokal yang menampilkan artikel seputar Ciamis (pemerintahan, ekonomi, olahraga, budaya, dll) untuk publik, dilengkapi panel admin untuk membuat, mengedit, dan menghapus berita.

## Tech Stack

| Layer | Teknologi | Alasan |
|---|---|---|
| Frontend | Nuxt 3 (Vue 3) | SSR/SSG bawaan — penting untuk SEO berita |
| Backend / DB | Supabase | Postgres, Auth, Storage, dan API otomatis dalam satu layanan |
| Autentikasi | Supabase Auth | Login admin (email/password) |
| Storage | Supabase Storage | Upload thumbnail/gambar berita |
| Deployment | Vercel atau Cloudflare Pages | Mendukung Nuxt 3 secara native |
| Editor konten | TipTap / Quill (rich text) | Editor WYSIWYG untuk penulisan berita |
| Anti-spam | Cloudflare Turnstile (gratis) | Proteksi form komentar dari bot/spam |
| SEO | Nuxt SEO module (`@nuxtjs/sitemap`, `useSeoMeta`) | Meta tag, sitemap, structured data |

## Arsitektur

```
Browser (pembaca & admin)
        │
        ▼
  Nuxt 3 App (Vercel / Cloudflare)
        │
        ▼
     Supabase
  (Auth, Database, Storage)
```

Frontend Nuxt berkomunikasi langsung ke Supabase menggunakan `@supabase/supabase-js`. Tidak ada backend custom terpisah — logic tambahan (generate slug, dsb) ditangani lewat Nuxt server routes (`server/api/`) yang berjalan sebagai serverless function saat deploy.

## Fitur

### Publik
- Beranda dengan daftar berita terbaru
- Halaman detail berita
- Filter berdasarkan kategori
- Filter/cari berdasarkan tags
- Pencarian berdasarkan kata kunci (full-text search)
- Pagination
- Penghitung jumlah dilihat (1 browser = 1 kali hitung per jam per berita)
- Tombol share (WhatsApp, Facebook, X, salin tautan)
- Related articles (berita lain dengan tag/kategori sama)
- Widget "berita terpopuler" (berdasarkan view_count)
- Kirim komentar (1 komentar per browser per berita)
- Edit komentar sendiri (masuk moderasi ulang setelah diedit)
- Lihat komentar yang sudah disetujui admin
- RSS feed

### Admin (setelah login)
- Login/logout (Supabase Auth)
- Buat berita baru (judul, konten, kategori, tags, thumbnail)
- Edit & hapus berita
- Simpan sebagai draft, publish, atau jadwalkan publish (scheduled)
- CRUD kategori (tambah, edit, hapus)
- CRUD tags (tambah, edit, hapus)
- Moderasi komentar: lihat antrian pending, approve/reject
- Statistik ringkas (jumlah dilihat per berita, jumlah komentar pending)

## Skema Database

### `articles`
| Kolom | Tipe | Keterangan |
|---|---|---|
| `id` | uuid | Primary key |
| `title` | text | Judul berita |
| `slug` | text | URL-friendly, unique, auto-generate dari title |
| `content` | text | Isi berita (markdown/rich text) |
| `thumbnail_url` | text | URL gambar dari Supabase Storage |
| `category_id` | uuid | Foreign key ke `categories` |
| `status` | text | `draft` atau `published` |
| `author_id` | uuid | Foreign key ke `auth.users` |
| `published_at` | timestamp | Waktu publish |
| `created_at` | timestamp | Waktu dibuat |

### `categories`
| Kolom | Tipe | Keterangan |
|---|---|---|
| `id` | uuid | Primary key |
| `name` | text | Contoh: Pemerintahan, Ekonomi, Olahraga, Budaya |
| `slug` | text | URL-friendly |

### `tags`
| Kolom | Tipe | Keterangan |
|---|---|---|
| `id` | uuid | Primary key |
| `name` | text | Contoh: pilkada, banjir, UMKM |
| `slug` | text | URL-friendly, unique |

### `article_tags` (tabel relasi many-to-many)
| Kolom | Tipe | Keterangan |
|---|---|---|
| `article_id` | uuid | Foreign key ke `articles` |
| `tag_id` | uuid | Foreign key ke `tags` |

### `article_views`
| Kolom | Tipe | Keterangan |
|---|---|---|
| `id` | uuid | Primary key |
| `article_id` | uuid | Foreign key ke `articles` |
| `visitor_id` | text | Identifier browser (disimpan di cookie/localStorage) |
| `viewed_at` | timestamp | Waktu dilihat |

Logika hitung dilihat: sebelum insert baris baru, cek apakah sudah ada baris dengan `article_id` + `visitor_id` yang sama dalam 1 jam terakhir. Kalau belum ada, insert baris baru dan tambahkan `articles.view_count` (kolom cache, di-update lewat Nuxt server route atau Supabase Edge Function). Kalau sudah ada, tidak dihitung lagi.

### `comments`
| Kolom | Tipe | Keterangan |
|---|---|---|
| `id` | uuid | Primary key |
| `article_id` | uuid | Foreign key ke `articles` |
| `visitor_id` | text | Identifier browser (sama seperti di atas) |
| `name` | text | Nama yang ditulis komentator (opsional/bebas isi) |
| `content` | text | Isi komentar |
| `status` | text | `pending` atau `approved` |
| `created_at` | timestamp | Waktu dibuat |
| `updated_at` | timestamp | Waktu terakhir diedit |

Constraint: `UNIQUE(article_id, visitor_id)` — 1 browser hanya bisa 1 komentar per berita. Alur moderasi:
1. Komentar baru masuk dengan `status = 'pending'`
2. Admin approve → `status = 'approved'` → langsung tampil di halaman detail berita
3. Kalau komentator edit komentar yang sudah approved → `status` balik jadi `pending`, komentar lama tetap tersembunyi sampai di-approve ulang

Catatan: identifikasi "1 browser" di sini pakai `visitor_id` yang di-generate dan disimpan di localStorage/cookie sisi client — cukup untuk mencegah spam kasual, tapi bisa di-bypass kalau user membersihkan data browser atau ganti browser. Untuk portofolio ini sudah memadai; kalau butuh lebih ketat, bisa ditambah verifikasi lain (misalnya rate-limit per IP di edge function).

### Row Level Security (RLS)
- **Publik**: hanya boleh `SELECT` artikel dengan `status = 'published'`; boleh `SELECT` komentar dengan `status = 'approved'`; boleh `INSERT` komentar baru dan `article_views`
- **Publik (pemilik komentar)**: boleh `UPDATE` komentar miliknya sendiri (dicocokkan lewat `visitor_id`) — update ini di-handle lewat Nuxt server route supaya sekaligus reset `status` jadi `pending`
- **Admin (authenticated)**: boleh `INSERT`, `UPDATE`, `DELETE` semua artikel, kategori, tags, dan boleh `UPDATE` status komentar (approve/reject)

## SEO

- Meta tag dinamis per halaman berita (`title`, `description`, `og:image`) pakai `useSeoMeta()` di Nuxt
- Structured data `schema.org/NewsArticle` untuk setiap halaman detail berita
- Sitemap otomatis (`@nuxtjs/sitemap`) dan `robots.txt`
- Canonical URL untuk menghindari duplicate content
- Slug URL yang deskriptif (sudah ada dari kolom `slug` di `articles`)
- Gambar thumbnail teroptimasi (lazy load, ukuran sesuai, `alt` text)

## Fitur Tambahan (opsional, nice-to-have)

- Full-text search Postgres untuk pencarian kata kunci yang lebih relevan
- RSS feed (`/rss.xml`) untuk pembaca/aggregator berita
- Widget berita terpopuler berdasarkan `view_count`
- Related articles berdasarkan tag/kategori yang sama
- Scheduled publish (artikel otomatis publish di waktu tertentu)
- Cloudflare Turnstile di form komentar untuk mengurangi spam/bot

## Struktur Folder (Nuxt 3, usulan)

```
ciamis-news/
├── pages/
│   ├── index.vue              # beranda
│   ├── berita/[slug].vue      # detail berita
│   ├── kategori/[slug].vue    # berita per kategori
│   └── admin/
│       ├── login.vue
│       ├── index.vue           # daftar berita (admin)
│       └── berita/
│           ├── baru.vue        # form tambah berita
│           └── [id]/edit.vue   # form edit berita
├── components/
│   ├── ArticleCard.vue
│   ├── ArticleEditor.vue
│   └── AdminSidebar.vue
├── composables/
│   └── useSupabase.ts
├── server/
│   └── api/                    # logic tambahan (mis. generate slug)
├── middleware/
│   └── auth.ts                 # proteksi halaman admin
└── nuxt.config.ts
```

## Roadmap Pengembangan

- [ ] Setup project Nuxt 3 + koneksi Supabase
- [ ] Buat tabel `articles`, `categories`, `tags`, `article_tags` + RLS policy
- [ ] Halaman publik: beranda, detail berita, kategori, tags
- [ ] Autentikasi admin
- [ ] CRUD berita di panel admin
- [ ] CRUD kategori & tags di panel admin
- [ ] Upload gambar ke Supabase Storage
- [ ] Search (kata kunci, kategori, tags) & pagination
- [ ] Fitur hitung dilihat (`article_views` + dedupe 1 jam)
- [ ] Tombol share sosial media
- [ ] Fitur komentar + alur moderasi admin
- [ ] Anti-spam (Cloudflare Turnstile) di form komentar
- [ ] Deploy ke Vercel/Cloudflare
- [ ] Optimasi SEO (meta tag, sitemap, structured data, OG image)

## Environment Variables

```
SUPABASE_URL=
SUPABASE_ANON_KEY=
```

## Catatan

Proyek ini dibuat untuk keperluan portofolio, menampilkan kemampuan membangun aplikasi full-stack sederhana-menengah dengan Vue/Nuxt ecosystem dan Backend-as-a-Service (Supabase).
