<script setup>
import { ref } from 'vue'

const categoryName = ref('Pemerintahan & Kebijakan')
const totalNews = ref(48)

// Filter Tab
const activeTab = ref('semua')
const tabs = [
    { id: 'semua', label: 'Semua' },
    { id: 'kebijakan', label: 'Kebijakan Daerah' },
    { id: 'infrastruktur', label: 'Infrastruktur' },
    { id: 'layanan', label: 'Layanan Publik' },
    { id: 'desa', label: 'Desa & Camat' }
]

// List Berita
const newsList = ref([
    {
        id: 1,
        title: 'Revitalisasi Kawasan Alun-Alun dan Masjid Agung...',
        excerpt: 'Pemugaran landmark kebanggaan tatar Galuh kini dilengkapi fasilitas...',
        badge: 'INFRASTRUKTUR',
        publishedAt: '06 Sep 2026 02.30',
        views: '4.8k',
        author: 'Biro Pemda',
        image: 'https://ak-d.tripcdn.com/images/0101912000stlh1qsDA2B_W_960_0_R5_Q60.webp?proc=source/trip'
    },
    {
        id: 2,
        title: 'Pemekaran Wilayah dan Pelayanan Adminduk Cepat',
        excerpt: 'Disdukcapil Kabupaten Ciamis meluncurkan loket jemput bola rekam...',
        badge: 'LAYANAN PUBLIK',
        publishedAt: '06 Sep 2026 01.15',
        views: '3.2k',
        author: 'Hendra Wijaya',
        image: 'https://images.unsplash.com/photo-1577495508048-b635879837f1?q=80&w=800&auto=format&fit=crop'
    },
    {
        id: 3,
        title: 'Pemkab Ciamis Salurkan Bantuan Beasiswa Prestasi...',
        excerpt: 'Total alokasi senilai 3,5 Milyar Rupiah diserahkan untuk ribuan peserta didik...',
        badge: 'KEBIJAKAN DAERAH',
        publishedAt: '05 Sep 2026 19.45',
        views: '2.7k',
        author: 'Biro Humas',
        image: 'https://images.unsplash.com/photo-1523240795612-9a054b0db644?q=80&w=800&auto=format&fit=crop'
    },
    {
        id: 4,
        title: 'Rapat Paripurna DPRD Ciamis Sahkan APBD 2025,',
        excerpt: 'Prioritas anggaran disepakati menitikberatkan infrastruktur...',
        badge: 'PEMERINTAHAN',
        publishedAt: '05 Sep 2026 14.20',
        views: '5.1k',
        author: 'Dedi Pratama',
        image: 'https://images.unsplash.com/photo-1517245386807-bb43f82c33c4?q=80&w=800&auto=format&fit=crop'
    },
    {
        id: 5,
        title: 'Proyek Bendungan Leuwikerang Ciamis...',
        excerpt: 'Balai Besar Wilayah Sungai memastikan tampungan air mampu...',
        badge: 'INFRASTRUKTUR',
        publishedAt: '04 Sep 2026 10.00',
        views: '6.4k',
        author: 'Biro Pemda',
        image: 'https://awsimages.detik.net.id/community/media/visual/2022/08/01/progres-pembangunan-bendungan-leuwikeris-4_169.jpeg?w=700&q=90'
    },
    {
        id: 6,
        title: 'Pemkab Ciamis Luncurkan Aplikasi SIAP-Ciamis untuk',
        excerpt: 'Integrasi NIB elektronik dan izin edar produk lokal kini selesai dalam...',
        badge: 'LAYANAN PUBLIK',
        publishedAt: '04 Sep 2026 08.10',
        views: '1.9k',
        author: 'Rina Astuti',
        image: 'https://images.unsplash.com/photo-1531482615713-2afd69097998?q=80&w=800&auto=format&fit=crop'
    },
    {
        id: 7,
        title: 'Dinas Sosial Ciamis Percepat Penyaluran Bansos Lansia...',
        excerpt: 'Skema pendampingan kesehatan door-to-door diperkuat oleh Tenaga...',
        badge: 'KEBIJAKAN DAERAH',
        publishedAt: '03 Sep 2026 16.30',
        views: '2.3k',
        author: 'Hendra Wijaya',
        image: 'https://images.unsplash.com/photo-1582213782179-e0d53f98f2ca?q=80&w=800&auto=format&fit=crop'
    },
    {
        id: 8,
        title: 'Bupati Ciamis Tinjau Kesiapan Tanggap Bencana',
        excerpt: 'Pos komando siaga 24 jam didirikan di wilayah rawan perbukitan dengan...',
        badge: 'PEMERINTAHAN',
        publishedAt: '03 Sep 2026 11.00',
        views: '3.8k',
        author: 'Biro Pemda',
        image: 'https://images.unsplash.com/photo-1509099836639-18ba1795216d?q=80&w=800&auto=format&fit=crop'
    },
    {
        id: 9,
        title: 'Kanal Pengaduan Ciamis Siaga 112 Catat 98% Respons',
        excerpt: 'Laporan darurat medis, pohon tumbang, serta perbaikan penerangan...',
        badge: 'LAYANAN PUBLIK',
        publishedAt: '02 Sep 2026 09.15',
        views: '4.1k',
        author: 'Dedi Pratama',
        image: 'https://images.unsplash.com/photo-1521791136064-7986c2920216?q=80&w=800&auto=format&fit=crop'
    }
])

// Trending List Sidebar
const trendingList = [
    { id: 1, title: 'Revitalisasi Kawasan Alun-Alun dan Masjid Agung Ciamis Resmi Dibuka', sub: 'Infrastruktur', views: '12.4k' },
    { id: 2, title: 'Rapat Paripurna DPRD Ciamis Sahkan Penetapan R-APBD Kabupaten 2025', sub: 'Anggaran', views: '9.8k' },
    { id: 3, title: 'Skema Baru Beasiswa Prestasi dan Bantuan UKT Mahasiswa Asal Ciamis', sub: 'Pendidikan', views: '7.2k' },
    { id: 4, title: 'Jadwal Layanan Keliling e-KTP dan Akta di Kecamatan Panumbangan & Kawali', sub: 'Layanan Publik', views: '6.5k' },
    { id: 5, title: 'Operasi Tanggap Cuaca Ekstrem Ciamis Utara: Nomor Hotline BPBD Aktif', sub: 'Kesiapsiagaan', views: '5.9k' }
]

const popularTags = [
    '#AlunAlunCiamis', '#BupatiCiamis', '#DPRDCiamis', '#RAPBD2025',
    '#InfrastrukturGaluh', '#PelayananPublik', '#BansosCiamis', '#TatarGaluh'
]
</script>

<template>
    <div class="bg-[#F8F9FA] min-h-screen font-sans text-gray-800 text-xs">
        <main class="max-w-7xl mx-auto space-y-6">

            <!-- Breadcrumb -->
            <div class="flex items-center gap-1.5 text-[11px] text-gray-500">
                <NuxtLink to="/" class="hover:text-[#A72185] flex items-center gap-1">
                    <svg class="w-3.5 h-3.5" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
                        <path
                            d="M3 12l2-2m0 0l7-7 7 7M5 10v10a1 1 0 001 1h3m10-11l2 2m-2-2v10a1 1 0 01-1 1h-3m-6 0a1 1 0 001-1v-4a1 1 0 011-1h2a1 1 0 011 1v4a1 1 0 001 1m-6 0h6" />
                    </svg>
                    Beranda
                </NuxtLink>
                <span>&rsaquo;</span>
                <span class="text-[#A72185] font-bold">{{ categoryName }}</span>
            </div>

            <!-- Header Banner Kanal (Disesuaikan dengan Desain) -->
            <div class="flex flex-col md:flex-row items-start md:items-center justify-between gap-4 py-2">
                <div class="space-y-1.5">
                    <div class="flex items-center gap-2">
                        <span
                            class="bg-[#A72185]/10 text-[#A72185] text-[10px] font-bold px-2 py-0.5 rounded tracking-wide">
                            KANAL DAERAH
                        </span>
                        <span class="text-gray-400 text-xs flex items-center gap-1">
                            •
                            <svg class="w-3.5 h-3.5 text-gray-500 inline" fill="none" stroke="currentColor"
                                stroke-width="2" viewBox="0 0 24 24">
                                <path stroke-linecap="round" stroke-linejoin="round"
                                    d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z" />
                            </svg>
                            Arsip Resmi Pemkab Ciamis
                        </span>
                    </div>
                    <h1 class="text-3xl font-extrabold text-gray-900 font-serif tracking-tight">
                        {{ categoryName }}
                    </h1>
                    <p class="text-gray-600 text-xs max-w-2xl leading-relaxed">
                        Kumpulan kabar, kebijakan bupati, transparansi anggaran, agenda DPRD, dan pembangunan fasilitas
                        publik di Kabupaten Ciamis dan sekitarnya.
                    </p>
                </div>

                <!-- Box Total Berita -->
                <div class="bg-[#F0F2F5] p-2.5 px-4 rounded-xl flex items-center gap-3 shrink-0">
                    <div class="w-9 h-9 rounded-lg bg-[#A72185] text-white flex items-center justify-center shrink-0">
                        <svg class="w-5 h-5" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
                            <path
                                d="M19 20H5a2 2 0 01-2-2V6a2 2 0 012-2h10a2 2 0 012 2v1m2 13a2 2 0 01-2-2V7m2 13a2 2 0 002-2V9a2 2 0 00-2-2h-2m-4-3H9M7 16h6M7 8h6v4H7V8z" />
                        </svg>
                    </div>
                    <div>
                        <div class="font-bold text-gray-900 text-sm leading-tight">{{ totalNews }} Berita</div>
                        <div class="text-[10px] text-gray-500">Terdata di Arsip Kanal</div>
                    </div>
                </div>
            </div>

            <!-- Tab Sub-Kategori & Sorting -->
            <div class="flex flex-col sm:flex-row items-start sm:items-center justify-between gap-4 pt-2">
                <div class="flex flex-wrap items-center gap-1.5">
                    <button v-for="t in tabs" :key="t.id" @click="activeTab = t.id" :class="[
                        'px-3.5 py-1.5 rounded-md font-bold transition text-[11px]',
                        activeTab === t.id ? 'bg-[#A72185] text-white' : 'bg-gray-200/70 text-gray-700 hover:bg-gray-300'
                    ]">
                        {{ t.label }}
                    </button>
                </div>

                <div class="flex items-center gap-2 text-gray-500 text-[11px]">
                    <span>Urutkan :</span>
                    <select
                        class="bg-gray-100 border border-transparent rounded-lg px-2.5 py-1 text-gray-800 font-semibold focus:outline-none">
                        <option>Terbaru (Default)</option>
                        <option>Terpopuler</option>
                    </select>
                </div>
            </div>

            <!-- Layout Grid Berita & Sidebar -->
            <div class="grid grid-cols-1 lg:grid-cols-12 gap-6 items-start pt-2">

                <!-- KIRI: Grid Card Berita (8 COLUMNS) -->
                <section class="lg:col-span-8 space-y-6">
                    <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-4">

                        <article v-for="item in newsList" :key="item.id"
                            class="bg-white rounded-lg border border-gray-200 overflow-hidden flex flex-col justify-between p-2.5">
                            <div class="space-y-2">
                                <div class="relative aspect-16/10 rounded overflow-hidden bg-gray-100">
                                    <img :src="item.image" :alt="item.title"
                                        class="w-full h-full object-cover hover:scale-105 transition duration-300" />
                                    <span
                                        class="absolute top-1.5 left-1.5 bg-[#A72185] text-white text-[8px] font-bold px-1.5 py-0.5 rounded uppercase tracking-wider">
                                        {{ item.badge }}
                                    </span>
                                </div>

                                <div class="flex items-center gap-2 text-[10px] text-gray-400 pt-1">
                                    <span class="flex items-center gap-1">
                                        <svg class="w-3 h-3 text-[#A72185] shrink-0" fill="none" stroke="currentColor"
                                            stroke-width="2" viewBox="0 0 24 24">
                                            <path stroke-linecap="round" stroke-linejoin="round"
                                                d="M8 7V3m8 4V3m-9 8h10M5 21h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v12a2 2 0 002 2z" />
                                        </svg>
                                        <time>{{ item.publishedAt }}</time>
                                    </span>
                                    <span>•</span>
                                    <span class="flex items-center gap-0.5">
                                        <svg class="w-3 h-3 text-gray-400 shrink-0" fill="none" stroke="currentColor"
                                            stroke-width="2" viewBox="0 0 24 24">
                                            <path stroke-linecap="round" stroke-linejoin="round"
                                                d="M15 12a3 3 0 11-6 0 3 3 0 016 0z" />
                                            <path stroke-linecap="round" stroke-linejoin="round"
                                                d="M2.458 12C3.732 7.943 7.523 5 12 5c4.478 0 8.268 2.943 9.542 7-1.274 4.057-5.064 7-9.542 7-4.477 0-8.268-2.943-9.542-7z" />
                                        </svg>
                                        {{ item.views }}
                                    </span>
                                </div>

                                <h3
                                    class="font-bold text-gray-900 text-xs line-clamp-2 leading-snug hover:text-[#A72185]">
                                    <a href="#">{{ item.title }}</a>
                                </h3>
                                <p class="text-gray-500 text-[10px] line-clamp-2 leading-relaxed">
                                    {{ item.excerpt }}
                                </p>
                            </div>

                            <div
                                class="pt-2 mt-2 border-t border-gray-100 flex items-center justify-between text-[10px]">
                                <span class="text-gray-400">Oleh : <strong class="text-gray-700">{{ item.author
                                }}</strong></span>
                                <a href="#" class="text-[#A72185] font-bold hover:underline">Baca Selengkapnya &rsaquo;</a>
                            </div>
                        </article>

                    </div>

                    <!-- Pagination -->
                    <div class="flex items-center justify-center gap-1.5 pt-4">
                        <button class="px-2.5 py-1 text-gray-400 font-medium hover:bg-gray-100 rounded">&lt;
                            Sebelumnya</button>
                        <button class="w-7 h-7 bg-[#A72185] text-white font-bold rounded">1</button>
                        <button
                            class="w-7 h-7 bg-white border border-gray-200 text-gray-700 font-medium rounded hover:bg-gray-50">2</button>
                        <button
                            class="w-7 h-7 bg-white border border-gray-200 text-gray-700 font-medium rounded hover:bg-gray-50">3</button>
                        <button
                            class="w-7 h-7 bg-white border border-gray-200 text-gray-700 font-medium rounded hover:bg-gray-50">4</button>
                        <span class="px-1 text-gray-400">...</span>
                        <button
                            class="w-7 h-7 bg-white border border-gray-200 text-gray-700 font-medium rounded hover:bg-gray-50">12</button>
                        <button class="px-2.5 py-1 text-gray-700 font-medium hover:bg-gray-100 rounded">Selanjutnya
                            &gt;</button>
                    </div>
                </section>

                <!-- KANAN: Sticky Sidebar Widgets (4 COLUMNS) -->
                <aside class="lg:col-span-4 sticky top-6 self-start space-y-4">

                    <!-- Widget 1: Jadwal Sholat -->
                    <div class="bg-white p-3.5 rounded-lg border border-gray-200 space-y-2.5 shadow-xs">
                        <div class="flex items-center justify-between border-b border-gray-100 pb-2">
                            <h4 class="font-bold text-gray-900 flex items-center gap-1.5">
                                <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 48 48">
                                    <path d="M0 0h48v48H0z" fill="none" />
                                    <path fill="none" stroke="#a72185" stroke-linecap="round" stroke-linejoin="round"
                                        d="M35.46 20.175v1.334m-1.713-1.334v1.334m-1.713-1.334v1.334m-1.714-1.334v1.334m-1.711-1.334v1.334m-1.714-1.334v1.334m-1.713-1.334v1.334m5.068-11.224c-1.093.913-1.615 1.681-3.406 2.73c-4.377 2.565-3.362 5.582-3.345 8.494m13.556 0c.017-2.912 1.032-5.93-3.346-8.495c-1.79-1.048-2.313-1.816-3.46-2.729V8.732m1.63-1.94A1.593 1.593 0 1 1 30.285 5.2h.002m2.783-3.726l.658 1.333l1.47.214l-1.063 1.038l.251 1.465l-1.316-.692l-1.316.692l.252-1.465l-1.064-1.038l1.47-.214zm-9.467 29.199v-7.386h13.443v9.68m-9.326 1.167v-3.516a2.434 2.434 0 0 1 2.44-2.44h.299a2.435 2.435 0 0 1 2.44 2.44v3.588M45.5 23.608a15.84 15.84 0 0 1-15.016 10.797m-7.107-1.68c-5.179-2.605-8.734-7.968-8.734-14.161A15.84 15.84 0 0 1 28.138 2.898M45.476 23.6q.004.204.004.409h0c0 11.868-9.62 21.49-21.489 21.49c-11.868 0-21.49-9.62-21.491-21.49h0c0-11.868 9.622-21.489 21.491-21.488h0c1.393 0 2.783.135 4.15.404" />
                                </svg>
                                Jadwal Shalat Ciamis
                            </h4>
                            <span class="text-[9px] text-gray-400 font-bold">WIB</span>
                        </div>
                        <div class="grid grid-cols-5 gap-1 text-center text-[9px]">
                            <div class="bg-gray-50 p-1 rounded">
                                <div class="text-gray-400">Subuh</div>
                                <div class="font-bold text-gray-800">04:15</div>
                            </div>
                            <div class="bg-pink-50 border border-pink-200 p-1 rounded">
                                <div class="text-[#A72185] font-bold">Dzuhur</div>
                                <div class="font-bold text-[#A72185]">11:42</div>
                            </div>
                            <div class="bg-gray-50 p-1 rounded">
                                <div class="text-gray-400">Ashar</div>
                                <div class="font-bold text-gray-800">14:55</div>
                            </div>
                            <div class="bg-gray-50 p-1 rounded">
                                <div class="text-gray-400">Maghrib</div>
                                <div class="font-bold text-gray-800">17:50</div>
                            </div>
                            <div class="bg-gray-50 p-1 rounded">
                                <div class="text-gray-400">Isya</div>
                                <div class="font-bold text-gray-800">19:01</div>
                            </div>
                        </div>
                        <p class="text-[8px] text-gray-400 text-center italic">Sumber: Kemenag Kab. Ciamis & DKM Masjid
                            Agung Ciamis</p>
                    </div>

                    <!-- Widget 2: Trending -->
                    <div class="bg-white p-3.5 rounded-lg border border-gray-200 space-y-3 shadow-xs">
                        <div class="flex items-center justify-between border-b border-gray-100 pb-2">
                            <h4 class="font-bold text-gray-900 flex items-center gap-1">
                                Trending di Kanal Ini
                            </h4>
                            <span class="bg-pink-100 text-[#A72185] text-[8px] font-bold px-1.5 py-0.5 rounded">TOP
                                5</span>
                        </div>

                        <div class="space-y-2.5">
                            <div v-for="(t, idx) in trendingList" :key="t.id" class="flex items-start gap-2.5">
                                <span class="text-base font-extrabold text-gray-300 leading-none">0{{ idx + 1 }}</span>
                                <div class="space-y-0.5">
                                    <a href="#"
                                        class="font-bold text-gray-800 hover:text-[#A72185] line-clamp-2 leading-snug">
                                        {{ t.title }}
                                    </a>
                                    <div class="text-[9px] text-gray-400">
                                        {{ t.sub }} • <span class="text-gray-500 font-medium">{{ t.views }}
                                            dibaca</span>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>

                    <!-- Widget 3: Tags Populer -->
                    <div class="bg-white p-3.5 rounded-lg border border-gray-200 space-y-2 shadow-xs">
                        <h4 class="font-bold text-gray-900 border-b border-gray-100 pb-2">Tags Populer Terkait</h4>
                        <div class="flex flex-wrap gap-1">
                            <a v-for="tag in popularTags" :key="tag" href="#"
                                class="bg-gray-100 hover:bg-[#A72185] hover:text-white text-gray-600 text-[10px] px-2 py-0.5 rounded transition">
                                {{ tag }}
                            </a>
                        </div>
                    </div>

                    <!-- Widget 4: Banner Partisipasi Publik -->
                    <div class="bg-[#A72185] p-4 rounded-lg text-white space-y-2 shadow-xs">
                        <div class="text-[9px] font-bold tracking-wider uppercase opacity-80">PARTISIPASI PUBLIK</div>
                        <h4 class="font-bold text-sm leading-snug">Punya Kabar Seputar Birokrasi atau Wilayah Desa Anda?
                        </h4>
                        <p class="text-[10px] opacity-90 leading-relaxed">Kirimkan siaran pers resmi, aspirasi warga,
                            atau agenda kegiatan masyarakat langsung ke meja redaksi kami.</p>
                        <button
                            class="w-full bg-white text-[#A72185] font-bold text-xs py-2 px-3 rounded mt-2 hover:bg-gray-100 transition flex items-center justify-center gap-1.5 cursor-pointer">
                            <svg class="w-3.5 h-3.5" fill="none" stroke="currentColor" stroke-width="2"
                                viewBox="0 0 24 24">
                                <path
                                    d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z" />
                            </svg>
                            <span>Kirim Siaran Pers</span>
                        </button>
                    </div>

                </aside>

            </div>

        </main>
    </div>
</template>