<template>
    <header class="w-full bg-white border-b border-gray-200 font-sans">
        <div class="max-w-7xl mx-auto px-4 py-4 space-y-4">

            <!-- Baris Atas: Logo & Info Meta -->
            <div class="flex flex-col lg:flex-row lg:items-center justify-between gap-4">

                <!-- Brand / Logo -->
                <div class="flex items-center gap-3">
                    <img src="/logo-ciamis.png" alt="Logo Kabupaten Ciamis" class="h-12 w-auto object-contain" />
                    <div>
                        <h1 class="text-2xl font-bold text-[#A72185] tracking-tight leading-none">
                            Ciamis News
                        </h1>
                        <p class="text-xs text-gray-500 font-normal mt-1">
                            Portal Informasi & Berita Tatar Galuh Ciamis
                        </p>
                    </div>
                </div>

                <!-- Info Meta -->
                <div class="flex flex-wrap items-center gap-x-4 gap-y-2 text-xs text-gray-500">

                    <!-- Tanggal -->
                    <div class="flex items-center gap-1.5">
                        <svg class="w-4 h-4 text-[#A72185]" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                d="M8 7V3m8 4V3m-9 8h10M5 21h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v12a2 2 0 002 2z" />
                        </svg>
                        <span class="uppercase tracking-wide font-medium text-gray-700">SENIN, 24 OKTOBER 2024</span>
                    </div>

                    <span class="text-gray-200 hidden sm:inline">|</span>

                    <!-- Cuaca / Suhu -->
                    <div class="flex items-center gap-1.5">
                        <svg class="w-4 h-4 text-[#A72185]" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                d="M12 3v1m0 16v1m9-9h-1M4 12H3m15.364 6.364l-.707-.707M6.343 6.343l-.707-.707m12.728 0l-.707.707M6.343 17.657l-.707.707M16 12a4 4 0 11-8 0 4 4 0 018 0z" />
                        </svg>
                        <span>Ciamis 28°C - Cerah Berawan</span>
                    </div>

                    <span class="text-gray-200 hidden sm:inline">|</span>

                    <!-- Kelembaban -->
                    <div class="flex items-center gap-1.5">
                        <svg xmlns="http://www.w3.org/2000/svg" width="14" height="14" viewBox="0 0 24 24">
                            <path d="M0 0h24v24H0z" fill="none" />
                            <mask id="SVGk33K9cMQ" width="18" height="22" x="3" y="1" fill="#000"
                                maskUnits="userSpaceOnUse">
                                <path fill="#fff" d="M3 1h18v22H3z" />
                                <path
                                    d="M19 14.571C19 18.121 15.866 21 12 21s-7-2.878-7-6.429c0-4.52 4.644-9.353 6.367-10.99a.913.913 0 0 1 1.266 0C14.356 5.217 19 10.05 19 14.57" />
                            </mask>
                            <g fill="none" stroke="#a72185">
                                <path stroke-width="4"
                                    d="M19 14.571C19 18.121 15.866 21 12 21s-7-2.878-7-6.429c0-4.52 4.644-9.353 6.367-10.99a.913.913 0 0 1 1.266 0C14.356 5.217 19 10.05 19 14.57Z"
                                    mask="url(#SVGk33K9cMQ)" />
                                <path stroke-linecap="round" stroke-width="2" d="M12 18a4 4 0 0 1-4-4" />
                            </g>
                        </svg>
                        <span>Kelembaban: 74%</span>
                    </div>

                    <span class="text-gray-200 hidden sm:inline">|</span>

                    <!-- Kecepatan Angin -->
                    <div class="flex items-center gap-1.5">
                        <svg class="w-4 h-4 text-[#A72185]" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                d="M9.59 4.59A2 2 0 1111 8H2m10.59 11.41A2 2 0 1014 16H2m15.73-8.27A2.5 2.5 0 1119.5 12H2" />
                        </svg>
                        <span>Angin: 9 km/jam</span>
                    </div>

                </div>

            </div>

            <!-- Baris Tengah: Split 2/3 untuk Search & 1/3 untuk Sekilas Info -->
            <div class="grid grid-cols-1 md:grid-cols-3 gap-4 items-center pt-1">

                <!-- Search Bar (Porsi 2/3) -->
                <div class="md:col-span-2 w-full">
                    <div
                        class="flex items-center bg-gray-50 border border-gray-200 rounded-lg overflow-hidden focus-within:border-[#A72185] transition">
                        <svg class="w-4 h-4 text-gray-400 ml-3 flex-shrink-0" fill="none" stroke="currentColor"
                            viewBox="0 0 24 24">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z" />
                        </svg>
                        <input type="text" placeholder="Cari arsip berita, regulasi pemkab, agenda daerah..."
                            class="w-full px-2.5 py-2 text-xs bg-transparent text-gray-800 placeholder-gray-400 focus:outline-none" />
                        <button
                            class="px-4 py-2 text-xs font-semibold text-[#A72185] hover:bg-gray-100 transition flex-shrink-0">
                            CARI
                        </button>
                    </div>
                </div>

                <!-- Sekilas Info Ticker (Porsi 1/3 dengan Truncate) -->
                <div class="md:col-span-1 w-full flex justify-end min-w-0">
                    <div
                        class="w-full bg-[#A72185]/10 text-[#A72185] px-3.5 py-2 rounded-lg flex items-center gap-2 text-xs font-semibold overflow-hidden">
                        <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24">
                            <path d="M0 0h24v24H0z" fill="none" />
                            <path fill="#a72185"
                                d="M18 7V3c0-.35-.19-.68-.49-.86a1 1 0 0 0-.99-.01L7.74 7H4c-1.1 0-2 .9-2 2v5c0 1.1.9 2 2 2h3v6h2v-5.46l7.59 3.37c.13.06.27.09.41.09a1.01 1.01 0 0 0 1-1v-4c2.21 0 4-1.79 4-4s-1.79-4-4-4M4 14V9h3v5zm12 3.46l-7-3.11V8.59l7-3.89zM18 13V9c1.1 0 2 .9 2 2s-.9 2-2 2" />
                        </svg>
                        <span class="truncate min-w-0">
                            <span class="font-bold">SEKILAS INFO:</span> Festival Seni Budaya Galuh Resmi Dibuka di
                            Situs Astana Gede
                        </span>
                    </div>
                </div>

            </div>

        </div>

        <!-- Baris Bawah: Navigation Menu -->
        <div class="bg-gray-50 border-t border-gray-200">
            <nav
                class="max-w-7xl mx-auto px-4 flex items-center gap-8 overflow-x-auto text-sm font-semibold text-gray-700">
                <NuxtLink to="/" class="py-3 text-[#A72185] border-b-2 border-[#A72185] whitespace-nowrap transition">
                    Berita Utama
                </NuxtLink>
                <NuxtLink to="/pemerintahan" class="py-3 hover:text-[#A72185] whitespace-nowrap transition">
                    Pemerintahan
                </NuxtLink>
                <NuxtLink to="/ekonomi" class="py-3 hover:text-[#A72185] whitespace-nowrap transition">
                    Ekonomi
                </NuxtLink>
                <NuxtLink to="/tatar-galuh" class="py-3 hover:text-[#A72185] whitespace-nowrap transition">
                    Tatar Galuh / Budaya
                </NuxtLink>
                <NuxtLink to="/pendidikan" class="py-3 hover:text-[#A72185] whitespace-nowrap transition">
                    Pendidikan & Olahraga
                </NuxtLink>
                <NuxtLink to="/wisata" class="py-3 hover:text-[#A72185] whitespace-nowrap transition">
                    Wisata & Kuliner
                </NuxtLink>
            </nav>
        </div>
    </header>
</template>