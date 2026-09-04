ciamis-news-vue/
├── app/                        # source code utama (konvensi Nuxt 4)
│   ├── app.vue                 # root component
│   ├── assets/
│   │   └── css/
│   │       └── main.css        # entry Tailwind (@import "tailwindcss")
│   ├── pages/                  # routing otomatis berdasarkan file
│   │   ├── index.vue
│   │   ├── berita/
│   │   │   └── [slug].vue
│   │   ├── kategori/
│   │   │   └── [slug].vue
│   │   └── admin/
│   │       ├── login.vue
│   │       ├── index.vue
│   │       └── berita/
│   │           ├── baru.vue
│   │           └── [id]/edit.vue
│   ├── components/
│   │   └── home/
│   │       ├── CitizenBanner.vue
│   │       └── HeroSection.vue
│   ├── layouts/
│   ├── composables/
│   │   └── useSupabase.ts
│   └── middleware/
│       └── auth.ts             # proteksi halaman admin
├── server/                     # API routes / server-side logic (tetap di root)
│   └── api/
├── public/                     # static assets (favicon, robots.txt, dll — tetap di root)
├── nuxt.config.ts
├── package.json
├── pnpm-lock.yaml
├── pnpm-workspace.yaml
├── tsconfig.json
├── brief_project.md
├── DESIGN.md
└── README.md

#CARA MENYIMPAM GAMBAR-GAMBAR :

public/ — untuk file statis yang diakses langsung by URL

Taruh di sini kalau filenya perlu diakses dengan URL tetap/dikenal, tanpa perlu di-import di kode. Cocok buat:

Logo Kabupaten Ciamis (dipakai di header, favicon, dll)
favicon.ico
robots.txt, sitemap.xml (kalau manual)
Gambar OG/share preview default
public/
├── favicon.ico
├── logo-ciamis.png
└── images/
    └── og-default.jpg

Cara akses di kode:

vue
<img src="/logo-ciamis.png" alt="Logo Kabupaten Ciamis" />

(Note: tanpa prefix public/ di path-nya, langsung /logo-ciamis.png — karena isi folder public otomatis jadi root URL)

app/assets/ — untuk aset yang diproses build tool (Vite)

Taruh di sini kalau gambar perlu di-optimize/bundling, atau dipakai di dalam CSS/SCSS:

app/assets/
├── css/
│   └── main.css
└── images/
    └── placeholder.png   # contoh: gambar fallback kalau thumbnail berita kosong

Cara akses di kode (Vue akan resolve & optimize otomatis):

vue
<img src="~/assets/images/placeholder.png" alt="Placeholder" />
Khusus untuk gambar berita (thumbnail, foto artikel)

Ini jangan taruh di public/ atau app/assets/ — karena itu untuk aset statis "bawaan" website, bukan konten dinamis. Foto berita yang di-upload admin harusnya masuk ke Supabase Storage (sesuai brief awal kita), lalu URL-nya disimpan di kolom thumbnail_url di database. Jadi alurnya: admin upload gambar → Supabase Storage → dapat URL → simpan URL itu ke tabel articles.