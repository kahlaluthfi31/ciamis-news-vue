# DESIGN.md — Ciamis News

## Product Overview
Ciamis News adalah portal berita online untuk wilayah Kabupaten Ciamis, Jawa Barat, Indonesia. Website ini menyajikan berita lokal (pemerintahan, ekonomi, olahraga, budaya, dll) untuk pembaca publik, dengan panel admin terpisah untuk mengelola konten.

## Brand Identity
- **Logo**: Lambang resmi Kabupaten Ciamis (lambang daerah berbentuk perisai/tameng khas heraldik Indonesia, berisi simbol-simbol daerah seperti gunung, padi-kapas, dan ornamen tradisional Sunda)
- **Primary color**: `#A72185` (ungu tua/magenta, diambil dari warna dominan logo)
- **Secondary color**: `#FFFFFF` (putih)
- Kombinasi warna harus terasa formal, terpercaya, dan khas institusi/berita daerah — bukan playful atau terlalu berwarna-warni. Ungu digunakan sebagai warna aksen kuat (header, tombol, kategori tag, garis pembatas), putih sebagai warna dominan background agar teks tetap mudah dibaca.

## Typography

**Font family**: **Inter** (Google Fonts, gratis) — dipakai untuk seluruh tampilan (heading & body), beda cuma di font-weight. Alasan: sangat readable untuk teks panjang, konsisten, ringan (satu font family aja, ga perlu load banyak font).

*(Alternatif kalau mau kesan lebih "koran/jurnalistik": tambah font serif seperti **Lora** khusus untuk H1/judul berita utama, tetap pakai Inter untuk sisanya.)*

**Type scale**:
| Elemen | Ukuran | Weight |
|---|---|---|
| H1 — judul berita utama | 32px | Bold (700) |
| H2 — judul section | 24px | Semibold (600) |
| H3 — judul card berita | 18px | Semibold (600) |
| Body — isi berita | 16px | Regular (400) |
| Small/caption — tanggal, views, meta | 14px | Regular (400) |

## Design Tokens Tambahan

**Spacing**
- Ikuti scale kelipatan 4px/8px (default Tailwind)
- Padding card: 16–24px
- Gap antar card di grid: 16–24px

**Border radius**
- Konsisten `rounded-lg` (8px) di semua card, button, dan input — hindari variasi radius yang beda-beda di elemen sejenis

**Warna semantik (selain primary/putih)**
- Teks sekunder (tanggal, meta info): abu-abu (`#6B7280` atau sejenis), agar tidak bersaing dengan judul
- Badge kategori: varian tint dari warna primary `#A72185` (opacity berbeda per kategori), atau 1 warna solid konsisten
- Status admin — draft: abu-abu, published: hijau, komentar pending: kuning/orange
- Border/divider: abu-abu terang (`#E5E7EB` atau sejenis)

**Icon set**
- Pakai satu library saja untuk konsistensi: **Lucide** atau **Heroicons** (keduanya gratis & ringan, cocok untuk Vue/Nuxt)

**Shadow/elevation**
- Maksimal 2 level shadow saja (misal: shadow tipis untuk card biasa, shadow lebih tegas untuk card yang di-hover/featured)

**Breakpoint responsive**
- Mobile: < 640px (prioritas utama, mobile-first)
- Tablet: 640px – 1024px
- Desktop: > 1024px

## Layout & Pages Needed

### 1. Homepage (Publik)
- Header: logo Kabupaten Ciamis + nama "Ciamis News", navigasi kategori, search bar
- Hero section: 1 berita utama (featured, gambar besar) + beberapa berita headline di sampingnya
- Grid daftar berita terbaru (card: thumbnail, judul, kategori tag, tanggal, jumlah dilihat)
- Sidebar: widget "Berita Terpopuler", daftar tags/kata kunci populer
- Footer: info website, kategori, tautan sosial media

### 2. Halaman Detail Berita
- Judul, tanggal publish, kategori, tags
- Gambar utama berita
- Isi berita (rich text)
- Jumlah dilihat (icon mata + angka)
- Tombol share (WhatsApp, Facebook, X, salin tautan)
- Related articles (berita lain dengan tag/kategori sama) di bagian bawah
- Section komentar: form kirim komentar + daftar komentar yang sudah disetujui

### 3. Halaman Kategori & Tags
- List berita yang difilter berdasarkan kategori atau tag tertentu, layout grid sama seperti homepage

### 4. Halaman Pencarian
- Search bar di atas, hasil pencarian dalam bentuk grid/list card berita

### 5. Panel Admin (setelah login)
- Halaman login sederhana (logo + form email/password)
- Dashboard: ringkasan jumlah berita, komentar pending
- Tabel daftar berita (dengan aksi edit/hapus, status draft/published)
- Form tambah/edit berita (input judul, kategori, tags, upload thumbnail, rich text editor konten, status draft/publish/scheduled)
- Halaman kelola kategori (CRUD sederhana: tabel + form)
- Halaman kelola tags (CRUD sederhana: tabel + form)
- Halaman moderasi komentar (daftar komentar pending dengan tombol approve/reject)

## Design Tone
Bersih, formal, terpercaya, mudah dibaca (readability tinggi untuk teks berita panjang). Terinspirasi dari portal berita daerah/nasional Indonesia — clean grid layout, whitespace cukup, kontras warna baik untuk aksesibilitas. Hindari desain yang terlalu ramai atau playful karena ini konten berita, bukan produk konsumer/e-commerce.

## Responsive
Harus mobile-first — mayoritas pembaca berita mengakses lewat HP.