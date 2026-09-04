<template>
    <footer class="bg-[#f0f4f9] text-gray-700 border-t border-gray-200/80 pt-10 pb-6 text-xs">
        <div class="max-w-7xl mx-auto px-4">
            <!-- Grid Utama 4 Kolom -->
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8 pb-8 border-b border-gray-200/80">

                <!-- Kolom 1: Brand & Tentang -->
                <div class="space-y-3">
                    <div class="flex items-center gap-2">
                        <img src="/logo-ciamis.png" alt="Logo Kabupaten Ciamis" class="h-8 w-auto object-contain" />
                        <span class="font-extrabold text-base text-[#A72185]">Ciamis News</span>
                    </div>
                    <p class="text-gray-600 leading-relaxed">
                        Portal Berita Resmi dan Media Edukasi Publik Kabupaten Ciamis. Menyajikan informasi
                        terverifikasi, aktual, berintegritas dan terpercaya untuk seluruh warga Tatar Galuh.
                    </p>
                    <!-- Social Icons Circular -->
                    <div class="flex items-center gap-2 pt-1">
                        <button
                            class="w-8 h-8 rounded-full bg-white border border-gray-200/80 text-gray-600 hover:text-[#A72185] hover:border-[#A72185] flex items-center justify-center transition shadow-2xs cursor-pointer"
                            aria-label="Share">
                            <svg class="w-3.5 h-3.5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                    d="M8.684 13.342C8.886 12.938 9 12.482 9 12c0-.482-.114-.938-.316-1.342m0 2.684a3 3 0 110-2.684m0 2.684l6.632 3.316m-6.632-6l6.632-3.316m0 0a3 3 0 105.367-2.684 3 3 0 00-5.367 2.684zm0 9.316a3 3 0 105.368 2.684 3 3 0 00-5.368-2.684z" />
                            </svg>
                        </button>
                        <button
                            class="w-8 h-8 rounded-full bg-white border border-gray-200/80 text-gray-600 hover:text-[#A72185] hover:border-[#A72185] flex items-center justify-center transition shadow-2xs cursor-pointer"
                            aria-label="RSS Feed">
                            <svg class="w-3.5 h-3.5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                    d="M6 5c7.18 0 13 5.82 13 13M6 11a7 7 0 017 7m-6 0a1 1 0 11-2 0 1 1 0 012 0z" />
                            </svg>
                        </button>
                        <button
                            class="w-8 h-8 rounded-full bg-white border border-gray-200/80 text-gray-600 hover:text-[#A72185] hover:border-[#A72185] flex items-center justify-center transition shadow-2xs cursor-pointer"
                            aria-label="Newsletter Email">
                            <svg class="w-3.5 h-3.5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                    d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z" />
                            </svg>
                        </button>
                        <button
                            class="w-8 h-8 rounded-full bg-white border border-gray-200/80 text-gray-600 hover:text-[#A72185] hover:border-[#A72185] flex items-center justify-center transition shadow-2xs cursor-pointer"
                            aria-label="Website">
                            <svg class="w-3.5 h-3.5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                    d="M21 12a9 9 0 01-9 9m9-9a9 9 0 00-9-9m9 9H3m9 9a9 9 0 01-9-9m9 9c1.657 0 3-4.03 3-9s-1.343-9-3-9m0 18c-1.657 0-3-4.03-3-9s1.343-9 3-9m-9 9a9 9 0 019-9" />
                            </svg>
                        </button>
                    </div>
                </div>

                <!-- Kolom 2: Kanal Berita -->
                <div class="space-y-3">
                    <div class="flex items-center gap-2 border-l-2 border-[#A72185] pl-2.5">
                        <h4 class="font-bold text-sm text-gray-900">Kanal Berita</h4>
                    </div>
                    <ul class="space-y-2 text-gray-600">
                        <li><a href="#" class="hover:text-[#A72185] transition">Berita Utama & Terkini</a></li>
                        <li><a href="#" class="hover:text-[#A72185] transition">Pemerintahan & Kebijakan</a></li>
                        <li><a href="#" class="hover:text-[#A72185] transition">Ekonomi, UMKM & Pasar</a></li>
                        <li><a href="#" class="hover:text-[#A72185] transition">Kebudayaan Tatar Galuh</a></li>
                        <li><a href="#" class="hover:text-[#A72185] transition">Pendidikan & PSGC Ciamis</a></li>
                        <li><a href="#" class="hover:text-[#A72185] transition">Destinasi Wisata & Kuliner Khas</a></li>
                    </ul>
                </div>

                <!-- Kolom 3: Pemerintah Kab. Ciamis -->
                <div class="space-y-3">
                    <div class="flex items-center gap-2 border-l-2 border-[#A72185] pl-2.5">
                        <h4 class="font-bold text-sm text-gray-900">Pemerintah Kab. Ciamis</h4>
                    </div>
                    <div class="space-y-1.5 text-gray-600 leading-relaxed">
                        <p class="font-bold text-gray-800">Gedung Bale Rancage & Kantor Bupati</p>
                        <p>Jl. Jendral Sudirman No. 16, Ciamis, Jawa Barat 46211</p>
                        <p><span class="text-gray-500">Telepon:</span> (0265) 771012 / 771034</p>
                        <p><span class="text-gray-500">Surel:</span> redaksi@ciamisnews.ciamiskab.go.id</p>
                        <p><span class="text-gray-500">PPID:</span> ppid@ciamiskab.go.id</p>
                    </div>
                    <div class="pt-1">
                        <span
                            class="inline-block bg-white border border-gray-200 text-gray-600 text-[10px] px-2.5 py-1 rounded shadow-2xs font-medium">
                            Verifikasi Dewan Pers ID: 46211/DP/2022
                        </span>
                    </div>
                </div>

                <!-- Kolom 4: Pedoman Media Siber -->
                <div class="space-y-3">
                    <div class="flex items-center gap-2 border-l-2 border-[#A72185] pl-2.5">
                        <h4 class="font-bold text-sm text-gray-900">Pedoman Media Siber</h4>
                    </div>
                    <p class="text-gray-600 leading-relaxed">
                        Seluruh konten berita, foto, infografis, dan video yang dipublikasikan Ciamis News dilindungi
                        hak cipta dan mentaati Kode Etik Jurnalistik serta Pedoman Pemberitaan Media Siber Dewan Pers.
                    </p>
                    <div class="flex items-center gap-2 text-[11px] font-bold text-[#A72185] pt-1">
                        <a href="#" class="hover:underline">Susunan Redaksi</a>
                        <span>•</span>
                        <a href="#" class="hover:underline">Hak Jawab</a>
                        <span>•</span>
                        <a href="#" class="hover:underline">Disclaimer</a>
                    </div>
                </div>

            </div>

            <!-- Bottom Bar (Copyright & Motto) -->
            <div class="pt-5 flex flex-col md:flex-row items-center justify-between gap-3 text-gray-500 text-[11px]">
                <p>© 2026 Dinas Komunikasi dan Informatika Kabupaten Ciamis. Hak Cipta Dilindungi Undang-Undang.</p>
                <span class="font-black text-[#A72185] tracking-wider uppercase">
                    CIAMIS BERKARAKTER & SEJAHTERA
                </span>
            </div>
        </div>
    </footer>
</template>