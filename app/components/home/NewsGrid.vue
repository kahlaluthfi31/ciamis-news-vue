<template>
    <div class="space-y-6">
        <!-- Header Section + Filter Kategori -->
        <div class="flex flex-col sm:flex-row sm:items-center justify-between gap-4">
            <div class="flex items-center gap-2">
                <span class="w-2.5 h-6 bg-[#A72185] rounded-sm"></span>
                <h2 class="text-xl font-bold text-gray-900 tracking-tight">
                    Berita Terkini Tatar Galuh
                </h2>
            </div>

            <!-- Filter Tabs -->
            <div class="flex items-center gap-1.5 overflow-x-auto text-xs font-semibold pb-1">
                <button class="bg-[#A72185] text-white px-3 py-1.5 rounded transition">Semua</button>
                <button
                    class="bg-gray-100 text-gray-700 hover:bg-gray-200 px-3 py-1.5 rounded transition">Pemerintahan</button>
                <button
                    class="bg-gray-100 text-gray-700 hover:bg-gray-200 px-3 py-1.5 rounded transition">Ekonomi</button>
                <button
                    class="bg-gray-100 text-gray-700 hover:bg-gray-200 px-3 py-1.5 rounded transition">Budaya</button>
                <button
                    class="bg-gray-100 text-gray-700 hover:bg-gray-200 px-3 py-1.5 rounded transition">Pariwisata</button>
            </div>
        </div>

        <!-- Grid Berita (2 Kolom di Desktop) -->
        <div class="grid grid-cols-1 md:grid-cols-2 gap-4">

            <!-- Card 1 (Budaya) -->
            <article
                class="bg-white border border-gray-200 rounded p-3 shadow-xs hover:shadow-md transition flex flex-col justify-between">
                <div>
                    <div class="relative w-full h-48 rounded overflow-hidden mb-3">
                        <img src="https://images.unsplash.com/photo-1533105079780-92b9be482077?q=80&w=600&auto=format&fit=crop"
                            alt="Festival Budaya"
                            class="w-full h-full object-cover hover:scale-105 transition duration-500" />
                        <span
                            class="absolute top-2 left-2 bg-[#A72185] text-white text-[10px] font-bold px-2 py-0.5 rounded">Budaya</span>
                    </div>
                    <div class="flex items-center gap-2 text-[11px] text-gray-400 mb-2">
                        <span class="flex items-center gap-1">
                            <svg class="w-3.5 h-3.5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                    d="M8 7V3m8 4V3m-9 8h10M5 21h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v12a2 2 0 002 2z" />
                            </svg>
                            24 Okt 2024
                        </span>
                        <span>•</span>
                        <span class="flex items-center gap-1">
                            <svg class="w-3.5 h-3.5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                    d="M15 12a3 3 0 11-6 0 3 3 0 016 0z" />
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                    d="M2.458 12C3.732 7.943 7.523 5 12 5c4.478 0 8.268 2.943 9.542 7-1.274 4.057-5.064 7-9.542 7-4.477 0-8.268-2.943-9.542-7z" />
                            </svg>
                            1.4k dilihat
                        </span>
                    </div>
                    <h3
                        class="font-bold text-gray-900 text-sm leading-snug mb-2 hover:text-[#A72185] transition cursor-pointer">
                        Festival Seni Helaran Budaya Galuh Siap Digelar di Situs Karangkamulyan
                    </h3>
                    <p class="text-xs text-gray-500 line-clamp-2 mb-4">
                        Dinas Kebudayaan, Kepemudaan dan Olahraga mengumumkan pagelaran akbar seni helaran tradisional
                        guna melestarikan jejak...
                    </p>
                </div>
                <div class="flex items-center justify-between text-[11px] pt-2.5 border-t border-gray-100">
                    <span class="text-gray-400">Oleh: <strong class="text-gray-700">Redaksi Budaya</strong></span>
                    <a href="#" class="text-[#A72185] font-bold hover:underline">Selengkapnya ›</a>
                </div>
            </article>

            <!-- Card 2 (Ekonomi) -->
            <article
                class="bg-white border border-gray-200 rounded p-3 shadow-xs hover:shadow-md transition flex flex-col justify-between">
                <div>
                    <div class="relative w-full h-48 rounded overflow-hidden mb-3">
                        <img src="https://images.unsplash.com/photo-1500937386664-56d1dfef3854?q=80&w=600&auto=format&fit=crop"
                            alt="Padi Organik"
                            class="w-full h-full object-cover hover:scale-105 transition duration-500" />
                        <span
                            class="absolute top-2 left-2 bg-[#A72185] text-white text-[10px] font-bold px-2 py-0.5 rounded">Ekonomi</span>
                    </div>
                    <div class="flex items-center gap-2 text-[11px] text-gray-400 mb-2">
                        <span class="flex items-center gap-1">
                            <svg class="w-3.5 h-3.5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                    d="M8 7V3m8 4V3m-9 8h10M5 21h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v12a2 2 0 002 2z" />
                            </svg>
                            24 Okt 2024
                        </span>
                        <span>•</span>
                        <span class="flex items-center gap-1">
                            <svg class="w-3.5 h-3.5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                    d="M15 12a3 3 0 11-6 0 3 3 0 016 0z" />
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                    d="M2.458 12C3.732 7.943 7.523 5 12 5c4.478 0 8.268 2.943 9.542 7-1.274 4.057-5.064 7-9.542 7-4.477 0-8.268-2.943-9.542-7z" />
                            </svg>
                            2.1k dilihat
                        </span>
                    </div>
                    <h3
                        class="font-bold text-gray-900 text-sm leading-snug mb-2 hover:text-[#A72185] transition cursor-pointer">
                        Dinas Pertanian Ciamis Genjot Produktivitas Padi Organik di Wilayah Banjarsari
                    </h3>
                    <p class="text-xs text-gray-500 line-clamp-2 mb-4">
                        Pengembangan klaster pertanian organik ramah lingkungan berhasil meningkatkan hasil panen petani
                        hingga 6,8 ton gabah...
                    </p>
                </div>
                <div class="flex items-center justify-between text-[11px] pt-2.5 border-t border-gray-100">
                    <span class="text-gray-400">Oleh: <strong class="text-gray-700">Warta Ekonomi</strong></span>
                    <a href="#" class="text-[#A72185] font-bold hover:underline">Selengkapnya ›</a>
                </div>
            </article>

            <!-- Card 3 (Olahraga) -->
            <article
                class="bg-white border border-gray-200 rounded p-3 shadow-xs hover:shadow-md transition flex flex-col justify-between">
                <div>
                    <div class="relative w-full h-48 rounded overflow-hidden mb-3">
                        <img src="https://galuh.id/wp-content/uploads/2026/06/PSGC-Ciamis-di-Championship-2026.webp"
                            alt="PSGC Ciamis"
                            class="w-full h-full object-cover hover:scale-105 transition duration-500" />
                        <span
                            class="absolute top-2 left-2 bg-[#A72185] text-white text-[10px] font-bold px-2 py-0.5 rounded">Olahraga</span>
                    </div>
                    <div class="flex items-center gap-2 text-[11px] text-gray-400 mb-2">
                        <span class="flex items-center gap-1">
                            <svg class="w-3.5 h-3.5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                    d="M8 7V3m8 4V3m-9 8h10M5 21h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v12a2 2 0 002 2z" />
                            </svg>
                            23 Okt 2024
                        </span>
                        <span>•</span>
                        <span class="flex items-center gap-1">
                            <svg class="w-3.5 h-3.5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                    d="M15 12a3 3 0 11-6 0 3 3 0 016 0z" />
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                    d="M2.458 12C3.732 7.943 7.523 5 12 5c4.478 0 8.268 2.943 9.542 7-1.274 4.057-5.064 7-9.542 7-4.477 0-8.268-2.943-9.542-7z" />
                            </svg>
                            3.5k dilihat
                        </span>
                    </div>
                    <h3
                        class="font-bold text-gray-900 text-sm leading-snug mb-2 hover:text-[#A72185] transition cursor-pointer">
                        PSGC Ciamis Matangkan Strategi Hadapi Laga Kandang Liga 3 di Stadion Galuh
                    </h3>
                    <p class="text-xs text-gray-500 line-clamp-2 mb-4">
                        Laskar Singacala fokus memperkuat koordinasi lini pertahanan dan penyelesaian akhir menjelang
                        duel krusial babak playoff...
                    </p>
                </div>
                <div class="flex items-center justify-between text-[11px] pt-2.5 border-t border-gray-100">
                    <span class="text-gray-400">Oleh: <strong class="text-gray-700">Rubrik Olahraga</strong></span>
                    <a href="#" class="text-[#A72185] font-bold hover:underline">Selengkapnya ›</a>
                </div>
            </article>

            <!-- Card 4 (Pemerintahan) -->
            <article
                class="bg-white border border-gray-200 rounded p-3 shadow-xs hover:shadow-md transition flex flex-col justify-between">
                <div>
                    <div class="relative w-full h-48 rounded overflow-hidden mb-3">
                        <img src="https://images.unsplash.com/photo-1577495508048-b635879837f1?q=80&w=600&auto=format&fit=crop"
                            alt="Adminduk Ciamis"
                            class="w-full h-full object-cover hover:scale-105 transition duration-500" />
                        <span
                            class="absolute top-2 left-2 bg-[#A72185] text-white text-[10px] font-bold px-2 py-0.5 rounded">Pemerintahan</span>
                    </div>
                    <div class="flex items-center gap-2 text-[11px] text-gray-400 mb-2">
                        <span class="flex items-center gap-1">
                            <svg class="w-3.5 h-3.5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                    d="M8 7V3m8 4V3m-9 8h10M5 21h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v12a2 2 0 002 2z" />
                            </svg>
                            23 Okt 2024
                        </span>
                        <span>•</span>
                        <span class="flex items-center gap-1">
                            <svg class="w-3.5 h-3.5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                    d="M15 12a3 3 0 11-6 0 3 3 0 016 0z" />
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                    d="M2.458 12C3.732 7.943 7.523 5 12 5c4.478 0 8.268 2.943 9.542 7-1.274 4.057-5.064 7-9.542 7-4.477 0-8.268-2.943-9.542-7z" />
                            </svg>
                            980 dilihat
                        </span>
                    </div>
                    <h3
                        class="font-bold text-gray-900 text-sm leading-snug mb-2 hover:text-[#A72185] transition cursor-pointer">
                        Pemekaran Wilayah dan Pelayanan Adminduk Cepat Terpadu di 27 Kecamatan
                    </h3>
                    <p class="text-xs text-gray-500 line-clamp-2 mb-4">
                        Disdukcapil Kabupaten Ciamis mengoperasikan layanan mobil keliling cetak KTP elektronik dan Akta
                        kelahiran langsung jadi...
                    </p>
                </div>
                <div class="flex items-center justify-between text-[11px] pt-2.5 border-t border-gray-100">
                    <span class="text-gray-400">Oleh: <strong class="text-gray-700">Biro Pemerintahan</strong></span>
                    <a href="#" class="text-[#A72185] font-bold hover:underline">Selengkapnya ›</a>
                </div>
            </article>

            <!-- Card 5 (Pariwisata) -->
            <article
                class="bg-white border border-gray-200 rounded p-3 shadow-xs hover:shadow-md transition flex flex-col justify-between">
                <div>
                    <div class="relative w-full h-48 rounded overflow-hidden mb-3">
                        <img src="https://images.unsplash.com/photo-1507525428034-b723cf961d3e?q=80&w=600&auto=format&fit=crop"
                            alt="Situ Lengkong Panjalu"
                            class="w-full h-full object-cover hover:scale-105 transition duration-500" />
                        <span
                            class="absolute top-2 left-2 bg-[#A72185] text-white text-[10px] font-bold px-2 py-0.5 rounded">Pariwisata</span>
                    </div>
                    <div class="flex items-center gap-2 text-[11px] text-gray-400 mb-2">
                        <span class="flex items-center gap-1">
                            <svg class="w-3.5 h-3.5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                    d="M8 7V3m8 4V3m-9 8h10M5 21h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v12a2 2 0 002 2z" />
                            </svg>
                            22 Okt 2024
                        </span>
                        <span>•</span>
                        <span class="flex items-center gap-1">
                            <svg class="w-3.5 h-3.5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                    d="M15 12a3 3 0 11-6 0 3 3 0 016 0z" />
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                    d="M2.458 12C3.732 7.943 7.523 5 12 5c4.478 0 8.268 2.943 9.542 7-1.274 4.057-5.064 7-9.542 7-4.477 0-8.268-2.943-9.542-7z" />
                            </svg>
                            2.8k dilihat
                        </span>
                    </div>
                    <h3
                        class="font-bold text-gray-900 text-sm leading-snug mb-2 hover:text-[#A72185] transition cursor-pointer">
                        Wisata Alam Situ Lengkong Panjalu Catat Kenaikan Kunjungan Wisatawan Akhir Pekan
                    </h3>
                    <p class="text-xs text-gray-500 line-clamp-2 mb-4">
                        Daya tarik ziarah Nusa Gede serta perahu wisata danau alami terus mendongkrak pendapatan
                        retribusi daerah dan ekonomi...
                    </p>
                </div>
                <div class="flex items-center justify-between text-[11px] pt-2.5 border-t border-gray-100">
                    <span class="text-gray-400">Oleh: <strong class="text-gray-700">Rubrik Wisata</strong></span>
                    <a href="#" class="text-[#A72185] font-bold hover:underline">Selengkapnya ›</a>
                </div>
            </article>

            <!-- Card 6 (Pendidikan) -->
            <article
                class="bg-white border border-gray-200 rounded p-3 shadow-xs hover:shadow-md transition flex flex-col justify-between">
                <div>
                    <div class="relative w-full h-48 rounded overflow-hidden mb-3">
                        <img src="https://images.unsplash.com/photo-1523240795612-9a054b0db644?q=80&w=600&auto=format&fit=crop"
                            alt="Beasiswa Ciamis"
                            class="w-full h-full object-cover hover:scale-105 transition duration-500" />
                        <span
                            class="absolute top-2 left-2 bg-[#A72185] text-white text-[10px] font-bold px-2 py-0.5 rounded">Pendidikan</span>
                    </div>
                    <div class="flex items-center gap-2 text-[11px] text-gray-400 mb-2">
                        <span class="flex items-center gap-1">
                            <svg class="w-3.5 h-3.5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                    d="M8 7V3m8 4V3m-9 8h10M5 21h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v12a2 2 0 002 2z" />
                            </svg>
                            22 Okt 2024
                        </span>
                        <span>•</span>
                        <span class="flex items-center gap-1">
                            <svg class="w-3.5 h-3.5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                    d="M15 12a3 3 0 11-6 0 3 3 0 016 0z" />
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                    d="M2.458 12C3.732 7.943 7.523 5 12 5c4.478 0 8.268 2.943 9.542 7-1.274 4.057-5.064 7-9.542 7-4.477 0-8.268-2.943-9.542-7z" />
                            </svg>
                            1.7k dilihat
                        </span>
                    </div>
                    <h3
                        class="font-bold text-gray-900 text-sm leading-snug mb-2 hover:text-[#A72185] transition cursor-pointer">
                        Pemkab Ciamis Salurkan Bantuan Beasiswa Prestasi untuk Siswa Berprestasi Tatar Galuh
                    </h3>
                    <p class="text-xs text-gray-500 line-clamp-2 mb-4">
                        Total dana stimulan pendidikan sebesar 3,2 miliar rupiah dialokasikan bagi ratusan santri, siswa
                        vokasi, dan mahasiswa...
                    </p>
                </div>
                <div class="flex items-center justify-between text-[11px] pt-2.5 border-t border-gray-100">
                    <span class="text-gray-400">Oleh: <strong class="text-gray-700">Redaksi Pendidikan</strong></span>
                    <a href="#" class="text-[#A72185] font-bold hover:underline">Selengkapnya ›</a>
                </div>
            </article>

        </div>

        <!-- Load More Button -->
        <div
            class="bg-white border border-gray-200 rounded p-3 flex flex-col sm:flex-row items-center justify-between gap-3 text-xs">
            <span class="text-gray-500">
                Menampilkan <strong>6</strong> dari <strong>148</strong> artikel terkini seputar Kabupaten Ciamis
            </span>
            <button
                class="bg-gray-50 hover:bg-gray-100 border border-gray-200 text-[#A72185] font-bold px-4 py-2 rounded flex items-center gap-2 transition cursor-pointer">
                <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                        d="M4 4v5h.582m15.356 2A8.001 8.001 0 004.582 9m0 0H9m11 11v-5h-.581m0 0a8.003 8.003 0 01-15.357-2m15.357 2H15" />
                </svg>
                Muat Berita Lainnya
            </button>
        </div>
    </div>
</template>