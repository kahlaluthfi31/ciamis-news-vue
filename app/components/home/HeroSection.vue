<template>
    <section class="max-w-7xl mx-auto py-1 font-sans">

        <!-- Label Section -->
        <div class="flex items-center gap-2 mb-4">
            <span class="w-2 h-2 rounded-full bg-[#A72185]"></span>
            <h2 class="text-xs font-bold text-[#A72185] tracking-wider uppercase">
                SOROTAN UTAMA HARI INI
            </h2>
        </div>

        <!-- Layout Grid: Kiri (Main Featured - 8 Col) & Kanan (Sticky Sidebar - 4 Col) -->
        <div class="grid grid-cols-1 lg:grid-cols-12 gap-6 items-start">

            <!-- ================= KONTEN UTAMA (KIRI - 8 COLUMNS) ================= -->
            <div class="lg:col-span-8 bg-white border border-gray-200 rounded p-3 md:p-6 shadow-xs">

                <!-- Thumbnail / Gambar Utama -->
                <div class="relative w-full h-[280px] sm:h-[380px] md:h-[420px] rounded-lg overflow-hidden mb-4">
                    <img src="https://ik.imagekit.io/tvlk/blog/2025/06/alun-alun-ciamis.jpg?tr=q-70,c-at_max,w-1000,h-600"
                        alt="Revitalisasi Alun-Alun Ciamis"
                        class="w-full h-full object-cover hover:scale-105 transition duration-500" />
                    <!-- Badge Kategori -->
                    <div
                        class="absolute top-3 left-3 bg-[#A72185] text-white text-xs font-bold px-3 py-1 rounded-lg uppercase tracking-wider">
                        PEMERINTAHAN
                    </div>
                </div>

                <!-- Meta Info (Penulis, Tanggal, Dibaca) -->
                <div class="flex flex-wrap items-center gap-x-4 gap-y-2 text-xs text-gray-500 mb-3">
                    <div class="flex items-center gap-1.5">
                        <svg class="w-4 h-4 text-gray-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                d="M19 20H5a2 2 0 01-2-2V6a2 2 0 012-2h10a2 2 0 012 2v1m2 13a2 2 0 01-2-2V7m2 13a2 2 0 002-2V9a2 2 0 00-2-2h-2m-4-3H9M7 16h6M7 8h6" />
                        </svg>
                        <span class="font-medium text-gray-700">Redaksi Ciamis News</span>
                    </div>
                    <span class="text-gray-300">•</span>
                    <div class="flex items-center gap-1.5">
                        <svg class="w-4 h-4 text-gray-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                d="M8 7V3m8 4V3m-9 8h10M5 21h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v12a2 2 0 002 2z" />
                        </svg>
                        <span>4 Sep 2026</span>
                    </div>
                    <span class="text-gray-300">•</span>
                    <div class="flex items-center gap-1.5">
                        <svg class="w-4 h-4 text-gray-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                d="M15 12a3 3 0 11-6 0 3 3 0 016 0z" />
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                d="M2.458 12C3.732 7.943 7.523 5 12 5c4.478 0 8.268 2.943 9.542 7-1.274 4.057-5.064 7-9.542 7-4.477 0-8.268-2.943-9.542-7z" />
                        </svg>
                        <span>4.8k Dibaca</span>
                    </div>
                </div>

                <!-- Judul Berita Utama (H1 - 32px sesuai design.md) -->
                <h1
                    class="text-xl sm:text-2xl md:text-[32px] font-bold text-gray-900 leading-snug mb-3 hover:text-[#A72185] transition cursor-pointer">
                    Revitalisasi Kawasan Alun-Alun dan Masjid Agung Ciamis Resmi Dibuka, Dorong Pusat Ekonomi Kreatif
                    Warga
                </h1>

                <!-- Deskripsi/Ringkasan -->
                <p class="text-sm md:text-base text-gray-600 leading-relaxed mb-6 font-normal">
                    Bupati Ciamis bersama jajaran Forkopimda secara resmi meresmikan wajah baru kawasan sentral
                    Alun-Alun dan pelataran Masjid Agung Ciamis. Revitalisasi ini mengintegrasikan ruang publik ramah
                    anak, pedestrian berarsitektur Sunda Galuh, serta galeri terkurasi bagi pelaku UMKM kuliner dan
                    kerajinan lokal khas Tatar Galuh.
                </p>

                <!-- Footer Card -->
                <div class="flex flex-wrap items-center justify-between gap-4 pt-4 border-t border-gray-100 text-xs">
                    <div class="flex items-center gap-1.5 text-gray-500 font-medium">
                        <svg class="w-4 h-4 text-[#A72185]" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z" />
                        </svg>
                        <span>Terverifikasi Dewan Pers & Protokol Redaksi</span>
                    </div>
                    <NuxtLink to="/berita/revitalisasi-alun-alun-ciamis"
                        class="flex items-center gap-1 font-bold text-[#A72185] hover:underline">
                        Baca Selengkapnya
                        <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                d="M14 5l7 7m0 0l-7 7m7-7H3" />
                        </svg>
                    </NuxtLink>
                </div>

            </div>

            <!-- ================= SIDEBAR BERITA PILIHAN (KANAN - 4 COLUMNS) ================= -->
            <!-- 'sticky top-6' MEMBUAT BAGIAN INI DIAM DITEMPAT SAAT DI-SCROLL -->
            <div class="lg:col-span-4 sticky top-6 self-start space-y-4">

                <!-- Box Wrapper Sidebar -->
                <div class="bg-white border border-gray-200 rounded overflow-hidden shadow-xs">

                    <!-- Header Tab Sidebar -->
                    <div class="bg-[#A72185] text-white px-4 py-3 flex items-center justify-between">
                        <div class="flex items-center gap-2">
                            <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                    d="M12 6.253v13m0-13C10.832 5.477 9.246 5 7.5 5S4.168 5.477 3 6.253v13C4.168 18.477 5.754 18 7.5 18s3.332.477 4.5 1.253m0-13C13.168 5.477 14.754 5 16.5 5c1.747 0 3.332.477 4.5 1.253v13C19.832 18.477 18.247 18 16.5 18c-1.746 0-3.332.477-4.5 1.253" />
                            </svg>
                            <h3 class="text-xs font-bold uppercase tracking-wider">
                                Berita Pilihan Redaksi
                            </h3>
                        </div>
                        <span class="text-[10px] bg-white/20 px-2 py-0.5 rounded text-white font-medium">
                            Galuh Update
                        </span>
                    </div>

                    <!-- Daftar Berita Pilihan (Maksimal 3 Berita) -->
                    <div class="divide-y divide-gray-100">

                        <!-- Item 1 -->
                        <div class="p-4 hover:bg-gray-50 transition flex gap-3 group cursor-pointer">
                            <img src="https://images.unsplash.com/photo-1606744837616-56c9a5c6a6eb?q=80&w=300&auto=format&fit=crop"
                                alt="Batik Ciamis"
                                class="w-20 h-20 rounded-lg object-cover flex-shrink-0 group-hover:opacity-90" />
                            <div class="flex flex-col justify-between flex-1 min-w-0">
                                <div>
                                    <span
                                        class="text-[10px] font-bold text-[#A72185] uppercase tracking-wider block mb-1">
                                        EKONOMI
                                    </span>
                                    <h4
                                        class="text-xs font-semibold text-gray-900 line-clamp-2 group-hover:text-[#A72185] transition leading-snug">
                                        Batik Khas Ciamis Rambah Pasar Ekspor, Omzet Pengrajin Melonjak
                                    </h4>
                                </div>
                                <div class="flex items-center gap-1 text-[11px] text-gray-400 mt-2">
                                    <svg class="w-3.5 h-3.5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                            d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z" />
                                    </svg>
                                    <span>2 jam yang lalu</span>
                                </div>
                            </div>
                        </div>

                        <!-- Item 2 -->
                        <div class="p-4 hover:bg-gray-50 transition flex gap-3 group cursor-pointer">
                            <img src="https://images.unsplash.com/photo-1544717305-2782549b5136?q=80&w=300&auto=format&fit=crop"
                                alt="Astana Gede"
                                class="w-20 h-20 rounded-lg object-cover flex-shrink-0 group-hover:opacity-90" />
                            <div class="flex flex-col justify-between flex-1 min-w-0">
                                <div>
                                    <span
                                        class="text-[10px] font-bold text-[#A72185] uppercase tracking-wider block mb-1">
                                        TATAR GALUH
                                    </span>
                                    <h4
                                        class="text-xs font-semibold text-gray-900 line-clamp-2 group-hover:text-[#A72185] transition leading-snug">
                                        Penataan Cagar Budaya Astana Gede Kawali Libatkan Sejarawan
                                    </h4>
                                </div>
                                <div class="flex items-center gap-1 text-[11px] text-gray-400 mt-2">
                                    <svg class="w-3.5 h-3.5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                            d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z" />
                                    </svg>
                                    <span>4 jam yang lalu</span>
                                </div>
                            </div>
                        </div>

                        <!-- Item 3 -->
                        <div class="p-4 hover:bg-gray-50 transition flex gap-3 group cursor-pointer">
                            <img src="https://images.unsplash.com/photo-1581092160607-ee22621dd758?q=80&w=300&auto=format&fit=crop"
                                alt="IoT Pertanian SMKN 1"
                                class="w-20 h-20 rounded-lg object-cover flex-shrink-0 group-hover:opacity-90" />
                            <div class="flex flex-col justify-between flex-1 min-w-0">
                                <div>
                                    <span
                                        class="text-[10px] font-bold text-[#A72185] uppercase tracking-wider block mb-1">
                                        PENDIDIKAN
                                    </span>
                                    <h4
                                        class="text-xs font-semibold text-gray-900 line-clamp-2 group-hover:text-[#A72185] transition leading-snug">
                                        SMKN 1 Ciamis Rintis Laboratorium IoT Pertanian Berbasis Modern
                                    </h4>
                                </div>
                                <div class="flex items-center gap-1 text-[11px] text-gray-400 mt-2">
                                    <svg class="w-3.5 h-3.5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                            d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z" />
                                    </svg>
                                    <span>6 jam yang lalu</span>
                                </div>
                            </div>
                        </div>

                    </div>

                </div>

            </div>

        </div>
    </section>
</template>