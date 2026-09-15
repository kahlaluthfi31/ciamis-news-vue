<script setup>
import { ref } from 'vue'

// const searchQuery = ref('Revitalisasi Alun-Alun')
const totalResults = ref(24)
const searchTime = ref('0.04')

// Filter Kategori/Tags Hasil Pencarian
const activeCategory = ref('semua')
const categories = [
    { id: 'semua', label: 'Semua', count: 24 },
    { id: 'infrastruktur', label: 'Infrastruktur', count: 11 },
    { id: 'pemerintahan', label: 'Pemerintahan', count: 7 },
    { id: 'ekonomi', label: 'Ekonomi & UKM', count: 4 },
    { id: 'seni', label: 'Seni & Budaya', count: 2 }
]

const selectedYear = ref('2024')
const sortBy = ref('Paling Relevan')
const viewMode = ref('list') // 'list' atau 'grid'

// Daftar Hasil Pencarian
const searchResults = ref([
    {
        id: 1,
        title: 'Revitalisasi Alun-Alun dan Kawasan Masjid Agung Ciamis Resmi Dibuka untuk Warga',
        excerpt: 'Proyek penataan menyeluruh kawasan inti Tatar Galuh resmi tuntas. Langkah revitalisasi alun-alun menghadirkan pedestrian ramah disabilitas, ruang edukasi sejarah kerajaan Galuh, dan taman...',
        badge: 'INFRASTRUKTUR PUBLIK',
        publishedAt: '24 Okt 2024, 09:30 WIB',
        views: '4.8k',
        author: 'Biro Liputan Daerah',
        image: 'https://images.unsplash.com/photo-1517245386807-bb43f82c33c4?q=80&w=800&auto=format&fit=crop'
    },
    {
        id: 2,
        title: 'Bupati Ciamis Tinjau Kesiapan Akhir Fasilitas Ramah Disabilitas di Alun-Alun Ciamis',
        excerpt: 'Memastikan hasil renovasi dapat dinikmati seluruh kalangan, jajaran Pemerintah Kabupaten Ciamis meninjau akses ramp kursi roda, guiding block tactile, serta sensor penerangan jalan umum...',
        badge: 'PEMERINTAHAN',
        publishedAt: '22 Okt 2024, 14:15 WIB',
        views: '3.1k',
        author: 'Dedi Hermansyah (Biro Pemda)',
        image: 'https://img.antarafoto.com/cache/1200x794/2020/07/07/minimnya-fasilitas-publik-ramah-disabilitas-qbeq-dom.webp'
    },
    {
        id: 3,
        title: 'Penataan PKL dan Sentra Kuliner Khas Galuh Pasca Revitalisasi Alun-Alun Diberlakukan',
        excerpt: 'Dinas KUKMP Ciamis menyediakan zona relokasi khusus yang lebih higienis dan representatif. Pedagang kuliner khas seperti tahu bulat, galendo, dan sate maranggi kini memiliki gerai berstandar...',
        badge: 'EKONOMI & UMKM',
        publishedAt: '20 Okt 2024, 18:40 WIB',
        views: '5.2k',
        author: 'Rina Puspitasari (Ekonomi & Bisnis)',
        image: 'https://asset.tribunnews.com/F-XgLu82Gk72Zb6fFwk-fSmQRHc=/1200x675/filters:upscale():quality(30):format(webp):focal(0.5x0.5:0.5x0.5)/jabar/foto/bank/originals/Pusat-Kuliner-Alun-Alun-Timur-Ciamis.jpg'
    },
    {
        id: 4,
        title: 'Dinas Perhubungan Ciamis Rekayasa Jalur Lalu Lintas Sekitar Kawasan',
        excerpt: 'Guna mengantisipasi lonjakan antusiasme masyarakat seusai serah terima revitalisasi alun-alun, Dishub memberlakukan sistem satu arah searah jarum jam pada ruas Jalan Perintis Kemerdekaan dan...',
        badge: 'LAYANAN PUBLIK',
        publishedAt: '18 Okt 2024, 08:00 WIB',
        views: '2.4k',
        author: 'Biro Publik & Transportasi',
        image: 'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRkTUCpWtVwsrH0PEgpG5wbihecXERZ-xk2mGSurlHGO9MzBmiqwK2TNmtI&s=10'
    },
    {
        id: 5,
        title: 'Antusiasme Warga Tatar Galuh Padati Ruang Terbuka Hijau Alun-Alun Ciamis di Akhir Pekan',
        excerpt: 'Wajah baru pusat kota menjadi daya tarik utama warga lokal maupun luar daerah. Komentar masyarakat menyambut gembira hasil revitalisasi alun-alun seraya menghimbau agar kesadaran...',
        badge: 'SUARA WARGA',
        publishedAt: '15 Okt 2024, 11:20 WIB',
        views: '6.1k',
        author: 'Hilman Suryana',
        image: 'https://images.unsplash.com/photo-1523240795612-9a054b0db644?q=80&w=800&auto=format&fit=crop'
    },
    {
        id: 6,
        title: 'DPRD Ciamis Apresiasi Pembangunan Ruang Publik Terintegrasi Alun-Alun dan Masjid Agung',
        excerpt: 'Komisi III DPRD Kabupaten Ciamis menggarisbawahi pentingnya alokasi biaya pemeliharaan berkelanjutan setelah proyek revitalisasi alun-alun...',
        badge: 'LEGISLATIF',
        publishedAt: '12 Okt 2024, 16:50 WIB',
        views: '1.9k',
        author: 'Warta Parlemen Ciamis',
        image: 'https://images.unsplash.com/photo-1517245386807-bb43f82c33c4?q=80&w=800&auto=format&fit=crop'
    }
])

// Sidebar Widget: Paling Banyak Dicari
const mostSearched = [
    { id: 1, title: 'Pilkada Ciamis 2024', searches: '12.4k penelusuran', count: '18 berita' },
    { id: 2, title: 'Beasiswa Mahasiswa Galuh Ciamis', searches: '8.9k penelusuran', count: '6 berita' },
    { id: 3, title: 'Jadwal Samsat Keliling Ciamis', searches: '7.2k penelusuran', category: 'Layanan Publik' },
    { id: 4, title: 'PSGC Ciamis Liga 3 Nasional', searches: '5.7k penelusuran', category: 'Olahraga' },
    { id: 5, title: 'Harga Beras & Cabai Pasar Manis', searches: '4.3k penelusuran', category: 'Pantauan Pasar' }
]

// Sidebar Widget: Arsip Berita Ciamis
const archiveMonths = [
    { name: 'Oktober', count: 82, active: true },
    { name: 'September', count: 114 },
    { name: 'Agustus', count: 96 },
    { name: 'Juli', count: 105 },
    { name: 'Juni', count: 88 },
    { name: 'Mei - Jan', count: 410 }
]

// Tags Pencarian Terkait
const relatedTags = [
    '# AlunAlunCiamis',
    '# TamanLokasana',
    '# MasjidAgungCiamis',
    '# StadionGaluh',
    '# RevitalisasiPasarManis',
    '# JembatanCirahong',
    '# SituLengkapPanjalu'
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
    <div class="bg-[#F8F9FB] min-h-screen font-sans text-gray-800 text-xs pb-12">
        <main class="max-w-7xl mx-auto sm:px-6 lg:px-8 space-y-2">

            <!-- Breadcrumb Navigation -->
            <nav class="flex items-center gap-2 text-[11px] text-gray-500">
                <NuxtLink to="/" class="hover:text-[#A72185] flex items-center gap-1 transition">
                    <svg class="w-3.5 h-3.5" fill="currentColor" viewBox="0 0 20 20">
                        <path
                            d="M10.707 2.293a1 1 0 00-1.414 0l-7 7a1 1 0 001.414 1.414L4 10.414V17a1 1 0 001 1h2a1 1 0 001-1v-2a1 1 0 011-1h2a1 1 0 011 1v2a1 1 0 001 1h2a1 1 0 001-1v-6.586l.293.293a1 1 0 001.414-1.414l-7-7z" />
                    </svg>
                    Beranda
                </NuxtLink>
                <span class="text-gray-400">&rsaquo;</span>
                <span class="text-gray-700 font-medium">Pencarian Arsip Berita</span>
            </nav>

            <!-- Main Search Bar Card -->
            <div class="bg-white p-5 rounded-sm
             border border-gray-200/80 shadow-xs space-y-4">
                <div class="flex items-center gap-3">
                    <div
                        class="flex-1 flex items-center gap-2 bg-gray-50/60 border border-gray-200 rounded-sm px-4 focus-within:border-[#A72185] focus-within:bg-white transition">
                        <!-- Icon Search -->
                        <svg class="w-5 h-5 text-[#9B1C70] shrink-0" fill="none" stroke="currentColor" stroke-width="2"
                            viewBox="0 0 24 24">
                            <path stroke-linecap="round" stroke-linejoin="round"
                                d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z" />
                        </svg>

                        <!-- Input Field -->
                        <input v-model="searchQuery" type="text"
                            class="flex-1 min-w-0 py-3 bg-transparent border-none text-sm text-slate-800 font-semibold placeholder-slate-400 focus:outline-none focus:ring-0"
                            placeholder="Revitalisasi Alun-Alun" />

                        <!-- Icon Clear / X -->
                        <button v-if="searchQuery" @click="searchQuery = ''" type="button"
                            class="text-slate-400 hover:text-slate-600 transition-colors shrink-0">
                            <svg class="w-4 h-4" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
                                <path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12" />
                            </svg>
                        </button>
                    </div>
                    <button
                        class="bg-[#A72185] hover:bg-[#8e1b70] text-white font-bold text-sm px-6 py-3 rounded-sm flex items-center gap-2 transition shrink-0 cursor-pointer shadow-xs">
                        <svg class="w-4 h-4" fill="none" stroke="currentColor" stroke-width="2" viewBox="0 0 24 24">
                            <path stroke-linecap="round" stroke-linejoin="round"
                                d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z" />
                        </svg>
                        <span>Cari Berita</span>
                    </button>
                </div>

                <!-- Search Metadata Stats & Actions -->
                <div class="flex items-center justify-between w-full pt-2 border-t border-gray-100 text-xs">

                    <!-- Bagian Kiri: Status & Kata Kunci -->
                    <div class="flex items-center gap-1.5 text-gray-600 flex-wrap">
                        <span class="w-2 h-2 rounded-full bg-emerald-500 inline-block shrink-0"></span>
                        <span>Menampilkan <strong>{{ totalResults }} hasil berita</strong> untuk kata kunci :</span>
                        <span class="bg-pink-100/70 text-[#A72185] font-bold px-2 py-0.5 rounded">
                            "{{ searchQuery }}"
                        </span>
                    </div>

                    <!-- Bagian Kanan: Waktu Pencarian (Pasti Rata Kanan) -->
                    <div class="text-gray-400 shrink-0 ml-4 whitespace-nowrap text-right">
                        Ditemukan dalam {{ searchTime }} detik
                    </div>

                </div>
            </div>

            <!-- Filter Category Bar & Sort Tools -->
            <div
                class="flex flex-col md:flex-row items-start md:items-center justify-between gap-3 bg-white p-3 rounded-sm border border-gray-200/80 shadow-xs">

                <!-- Category Filter Tabs -->
                <div class="flex flex-wrap items-center gap-1.5">
                    <span class="text-gray-500 font-medium text-[11px] mr-1">Kategori :</span>
                    <button v-for="cat in categories" :key="cat.id" @click="activeCategory = cat.id" :class="[
                        'px-3.5 py-1.5 rounded-md font-bold transition text-[11px] flex items-center gap-1',
                        activeCategory === cat.id
                            ? 'bg-[#A72185] text-white shadow-xs'
                            : 'bg-gray-200/70 text-gray-700 hover:bg-gray-300'
                    ]">
                        <span>{{ cat.label }}</span>
                        <span :class="activeCategory === cat.id ? 'text-pink-100' : 'text-gray-500 font-normal'">
                            ({{ cat.count }})
                        </span>
                    </button>
                </div>

                <!-- Year Filter, Sorting & View Toggle -->
                <div class="flex items-center gap-2 self-end md:self-auto text-[11px]">

                    <!-- Year Dropdown -->
                    <div class="relative flex items-center bg-gray-100 rounded-md px-2.5 py-1">
                        <svg class="w-3.5 h-3.5 text-gray-500 mr-1 shrink-0" fill="none" stroke="currentColor"
                            stroke-width="2" viewBox="0 0 24 24">
                            <path stroke-linecap="round" stroke-linejoin="round"
                                d="M8 7V3m8 4V3m-9 8h10M5 21h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v12a2 2 0 002 2z" />
                        </svg>
                        <select v-model="selectedYear"
                            class="bg-transparent border-none text-gray-700 font-medium focus:outline-none cursor-pointer p-0 text-[11px]">
                            <option value="2024">Tahun 2024</option>
                            <option value="2023">Tahun 2023</option>
                            <option value="2022">Tahun 2022 & Sebelumnya</option>
                        </select>
                    </div>

                    <!-- Sort Dropdown -->
                    <div class="relative flex items-center bg-gray-100 rounded-md px-2.5 py-1">
                        <svg class="w-3.5 h-3.5 text-gray-500 mr-1 shrink-0" fill="none" stroke="currentColor"
                            stroke-width="2" viewBox="0 0 24 24">
                            <path stroke-linecap="round" stroke-linejoin="round"
                                d="M3 4h13M3 8h9m-9 4h6m4 0l4-4m0 0l4 4m-4-4v12" />
                        </svg>
                        <select v-model="sortBy"
                            class="bg-transparent border-none text-gray-700 font-medium focus:outline-none cursor-pointer p-0 text-[11px]">
                            <option value="Paling Relevan">Paling Relevan</option>
                            <option value="Terbaru">Terbaru</option>
                            <option value="Terpopuler">Terpopuler</option>
                        </select>
                    </div>

                    <!-- Toggle View Button -->
                    <div class="flex items-center bg-gray-100 rounded-md p-0.5 border border-transparent">
                        <button @click="viewMode = 'list'"
                            :class="['p-1 rounded transition', viewMode === 'list' ? 'bg-white text-[#A72185] shadow-xs' : 'text-gray-400 hover:text-gray-600']"
                            title="Tampilan List">
                            <svg class="w-3.5 h-3.5" fill="none" stroke="currentColor" stroke-width="2"
                                viewBox="0 0 24 24">
                                <path stroke-linecap="round" stroke-linejoin="round" d="M4 6h16M4 12h16M4 18h16" />
                            </svg>
                        </button>
                        <button @click="viewMode = 'grid'"
                            :class="['p-1 rounded transition', viewMode === 'grid' ? 'bg-white text-[#A72185] shadow-xs' : 'text-gray-400 hover:text-gray-600']"
                            title="Tampilan Grid">
                            <svg class="w-3.5 h-3.5" fill="none" stroke="currentColor" stroke-width="2"
                                viewBox="0 0 24 24">
                                <path stroke-linecap="round" stroke-linejoin="round"
                                    d="M4 6a2 2 0 012-2h2a2 2 0 012 2v2a2 2 0 01-2 2H6a2 2 0 01-2-2V6zM14 6a2 2 0 012-2h2a2 2 0 012 2v2a2 2 0 01-2 2h-2a2 2 0 01-2-2V6zM4 16a2 2 0 012-2h2a2 2 0 012 2v2a2 2 0 01-2 2H6a2 2 0 01-2-2v-2zM14 16a2 2 0 012-2h2a2 2 0 012 2v2a2 2 0 01-2 2h-2a2 2 0 01-2-2v-2z" />
                            </svg>
                        </button>
                    </div>

                </div>
            </div>

            <!-- Main Content Layout (Result List + Sidebar) -->
            <div class="grid grid-cols-1 lg:grid-cols-12 gap-5 items-start">

                <!-- KIRI: Daftar Hasil Pencarian (8 COLUMNS) -->
                <section class="lg:col-span-8 space-y-3.5">

                    <!-- Item Berita List Format -->
                    <div v-if="viewMode === 'list'" class="space-y-3.5">
                        <article v-for="item in searchResults" :key="item.id"
                            class="bg-white rounded-sm
                             border border-gray-200/80 p-3.5 hover:shadow-md transition duration-200 flex flex-col sm:flex-row gap-4 group">
                            <!-- Image Thumbnail -->
                            <div class="sm:w-52 h-36 shrink-0 rounded-sm overflow-hidden relative bg-gray-100">
                                <img :src="item.image" :alt="item.title"
                                    class="w-full h-full object-cover group-hover:scale-105 transition duration-300" />
                            </div>

                            <!-- Content Body -->
                            <div class="flex-1 flex flex-col justify-between space-y-1.5">
                                <div class="space-y-1.5">
                                    <!-- Category Badge & Meta Info -->
                                    <div class="flex flex-wrap items-center gap-2 text-[10px]">
                                        <span
                                            class="bg-pink-100/80 text-[#A72185] font-extrabold px-2 py-0.5 rounded tracking-wide uppercase">
                                            {{ item.badge }}
                                        </span>
                                        <span class="text-gray-300">&bull;</span>
                                        <span class="text-gray-400 flex items-center gap-1">
                                            <svg class="w-3 h-3 text-gray-400" fill="none" stroke="currentColor"
                                                stroke-width="2" viewBox="0 0 24 24">
                                                <path stroke-linecap="round" stroke-linejoin="round"
                                                    d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z" />
                                            </svg>
                                            {{ item.publishedAt }}
                                        </span>
                                        <span class="text-gray-300">&bull;</span>
                                        <span class="text-gray-400 flex items-center gap-0.5">
                                            <svg class="w-3 h-3 text-gray-400" fill="none" stroke="currentColor"
                                                stroke-width="2" viewBox="0 0 24 24">
                                                <path stroke-linecap="round" stroke-linejoin="round"
                                                    d="M15 12a3 3 0 11-6 0 3 3 0 016 0z" />
                                                <path stroke-linecap="round" stroke-linejoin="round"
                                                    d="M2.458 12C3.732 7.943 7.523 5 12 5c4.478 0 8.268 2.943 9.542 7-1.274 4.057-5.064 7-9.542 7-4.477 0-8.268-2.943-9.542-7z" />
                                            </svg>
                                            {{ item.views }} dibaca
                                        </span>
                                    </div>

                                    <!-- Title with Highlighted Term -->
                                    <h3
                                        class="font-bold text-gray-900 text-sm group-hover:text-[#A72185] transition leading-snug">
                                        <NuxtLink :to="`/berita/${item.id}`">
                                            <template
                                                v-for="(part, i) in item.title.split(/(Revitalisasi Alun-Alun|Alun-Alun Ciamis)/g)"
                                                :key="i">
                                                <mark
                                                    v-if="part === 'Revitalisasi Alun-Alun' || part === 'Alun-Alun Ciamis'"
                                                    class="bg-pink-100 text-[#A72185] font-bold px-0.5 rounded">
                                                    {{ part }}
                                                </mark>
                                                <span v-else>{{ part }}</span>
                                            </template>
                                        </NuxtLink>
                                    </h3>

                                    <!-- Excerpt with Highlighted Term -->
                                    <p class="text-gray-500 text-[11px] line-clamp-2 leading-relaxed">
                                        <template
                                            v-for="(part, i) in item.excerpt.split(/(revitalisasi alun-alun|alun-alun)/g)"
                                            :key="i">
                                            <mark v-if="part === 'revitalisasi alun-alun' || part === 'alun-alun'"
                                                class="bg-pink-100 text-[#A72185] font-semibold px-0.5 rounded">
                                                {{ part }}
                                            </mark>
                                            <span v-else>{{ part }}</span>
                                        </template>
                                    </p>
                                </div>

                                <!-- Footer Author & Read More -->
                                <div
                                    class="flex items-center justify-between pt-2 border-t border-gray-100 text-[10px]">
                                    <span class="text-gray-400">
                                        Oleh: <strong class="text-gray-600 font-medium">{{ item.author }}</strong>
                                    </span>
                                    <NuxtLink :to="`/berita/${item.id}`"
                                        class="text-[#A72185] font-bold hover:underline flex items-center gap-0.5">
                                        <span>Baca Selengkapnya</span>
                                    </NuxtLink>
                                </div>
                            </div>
                        </article>
                    </div>

                    <!-- Item Berita Grid Format Alternative -->
                    <div v-else class="grid grid-cols-1 sm:grid-cols-2 gap-3.5">
                        <article v-for="item in searchResults" :key="item.id"
                            class="bg-white rounded-sm
                             border border-gray-200/80 overflow-hidden flex flex-col justify-between p-3 hover:shadow-md transition duration-200 group">
                            <div class="space-y-2">
                                <div class="aspect-16/10 rounded-sm overflow-hidden relative bg-gray-100">
                                    <img :src="item.image" :alt="item.title"
                                        class="w-full h-full object-cover group-hover:scale-105 transition duration-300" />
                                    <span
                                        class="absolute top-2 left-2 bg-[#A72185] text-white text-[8px] font-bold px-1.5 py-0.5 rounded uppercase">
                                        {{ item.badge }}
                                    </span>
                                </div>
                                <div class="flex items-center gap-2 text-[10px] text-gray-400 pt-0.5">
                                    <span>{{ item.publishedAt }}</span>
                                    <span>&bull;</span>
                                    <span>{{ item.views }} dibaca</span>
                                </div>
                                <h3
                                    class="font-bold text-gray-900 text-xs line-clamp-2 leading-snug group-hover:text-[#A72185]">
                                    {{ item.title }}
                                </h3>
                                <p class="text-gray-500 text-[10px] line-clamp-2 leading-relaxed">
                                    {{ item.excerpt }}
                                </p>
                            </div>
                            <div
                                class="pt-2 mt-2 border-t border-gray-100 flex items-center justify-between text-[10px]">
                                <span class="text-gray-400">Oleh : <strong class="text-gray-600">{{ item.author
                                        }}</strong></span>
                                <NuxtLink :to="`/berita/${item.id}`" class="text-[#A72185] font-bold hover:underline">
                                    &rarr;</NuxtLink>
                            </div>
                        </article>
                    </div>

                    <!-- Pagination Bar -->
                    <div class="bg-white p-3 rounded-sm
                         border border-gray-200/80 flex items-center justify-between text-[11px] text-gray-600">
                        <span class="text-gray-500">Menampilkan <strong>1 - 6</strong> dari 24 berita</span>
                        <div class="flex items-center gap-1">
                            <button disabled class="px-2.5 py-1 text-gray-300 font-medium cursor-not-allowed">&lsaquo;
                                Sebelumnya</button>
                            <button class="w-7 h-7 bg-[#A72185] text-white font-bold rounded-sm shadow-2xs">1</button>
                            <button
                                class="w-7 h-7 bg-white border border-gray-200 text-gray-700 font-medium rounded-sm hover:bg-gray-50">2</button>
                            <button
                                class="w-7 h-7 bg-white border border-gray-200 text-gray-700 font-medium rounded-sm hover:bg-gray-50">3</button>
                            <button
                                class="w-7 h-7 bg-white border border-gray-200 text-gray-700 font-medium rounded-sm hover:bg-gray-50">4</button>
                            <button
                                class="px-2.5 py-1 text-gray-700 font-medium hover:bg-gray-100 rounded-sm">Berikutnya
                                &rsaquo;</button>
                        </div>
                    </div>

                    <!-- Tags Pencarian Terkait Section -->
                    <div class="bg-white p-4 rounded-sm
                     border border-gray-200/80 space-y-2.5 shadow-xs">
                        <h4 class="font-bold text-gray-900 text-xs flex items-center gap-1.5">
                            <svg class="w-4 h-4 text-[#A72185]" fill="none" stroke="currentColor" stroke-width="2"
                                viewBox="0 0 24 24">
                                <path stroke-linecap="round" stroke-linejoin="round"
                                    d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z" />
                            </svg>
                            <span>Pencarian Terkait Galuh & Ciamis</span>
                        </h4>
                        <div class="flex flex-wrap gap-1.5">
                            <NuxtLink v-for="tag in relatedTags" :key="tag" to="#"
                                class="bg-gray-100 hover:bg-[#A72185] hover:text-white text-gray-600 text-[11px] px-2.5 py-1 rounded-md transition font-medium">
                                {{ tag }}
                            </NuxtLink>
                        </div>
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