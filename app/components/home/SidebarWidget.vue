<template>
    <aside class="space-y-5">
        <!-- Jadwal Sholat Widget -->
        <div class="bg-white rounded p-3 border border-gray-200 shadow-xs">
            <div
                class="border-b border-gray-200 pb-2 mb-2.5 flex justify-between items-center text-xs font-bold text-gray-800">
                <span class="flex items-center gap-1.5">
                    <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 48 48">
                        <path d="M0 0h48v48H0z" fill="none" />
                        <path fill="none" stroke="#a72185" stroke-linecap="round" stroke-linejoin="round"
                            d="M35.46 20.175v1.334m-1.713-1.334v1.334m-1.713-1.334v1.334m-1.714-1.334v1.334m-1.711-1.334v1.334m-1.714-1.334v1.334m-1.713-1.334v1.334m5.068-11.224c-1.093.913-1.615 1.681-3.406 2.73c-4.377 2.565-3.362 5.582-3.345 8.494m13.556 0c.017-2.912 1.032-5.93-3.346-8.495c-1.79-1.048-2.313-1.816-3.46-2.729V8.732m1.63-1.94A1.593 1.593 0 1 1 30.285 5.2h.002m2.783-3.726l.658 1.333l1.47.214l-1.063 1.038l.251 1.465l-1.316-.692l-1.316.692l.252-1.465l-1.064-1.038l1.47-.214zm-9.467 29.199v-7.386h13.443v9.68m-9.326 1.167v-3.516a2.434 2.434 0 0 1 2.44-2.44h.299a2.435 2.435 0 0 1 2.44 2.44v3.588M45.5 23.608a15.84 15.84 0 0 1-15.016 10.797m-7.107-1.68c-5.179-2.605-8.734-7.968-8.734-14.161A15.84 15.84 0 0 1 28.138 2.898M45.476 23.6q.004.204.004.409h0c0 11.868-9.62 21.49-21.489 21.49c-11.868 0-21.49-9.62-21.491-21.49h0c0-11.868 9.622-21.489 21.491-21.488h0c1.393 0 2.783.135 4.15.404" />
                    </svg>
                    Jadwal Shalat Ciamis
                </span>
                <span class="text-[10px] text-gray-400 font-normal">WIB</span>
            </div>
            <div class="grid grid-cols-5 gap-1 text-center text-[10px]">
                <div class="bg-gray-50 p-1.5 rounded">
                    <p class="text-gray-400">Subuh</p>
                    <p class="font-bold text-gray-800">04:18</p>
                </div>
                <div class="bg-gray-50 p-1.5 rounded">
                    <p class="text-gray-400">Dzuhur</p>
                    <p class="font-bold text-gray-800">11:45</p>
                </div>
                <div class="bg-[#A72185] text-white p-1.5 rounded">
                    <p class="opacity-80">Ashar</p>
                    <p class="font-bold">14:58</p>
                </div>
                <div class="bg-gray-50 p-1.5 rounded">
                    <p class="text-gray-400">Maghrib</p>
                    <p class="font-bold text-gray-800">17:50</p>
                </div>
                <div class="bg-gray-50 p-1.5 rounded">
                    <p class="text-gray-400">Isya</p>
                    <p class="font-bold text-gray-800">19:01</p>
                </div>
            </div>
        </div>

        <!-- Trending Top 5 -->
        <div class="bg-white rounded p-3 border border-gray-200 shadow-xs">
            <div class="flex justify-between items-center border-b border-gray-200 pb-2 mb-3">
                <h3 class="text-xs font-bold text-gray-900 flex items-center gap-1">
                    <svg class="w-4 h-4 text-[#A72185]" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                            d="M13 7h8m0 0v8m0-8l-8 8-4-4-6 6" />
                    </svg>
                    Trending Tatar Galuh
                </h3>
                <span class="text-[10px] text-[#A72185] font-semibold cursor-pointer hover:underline">Lihat Semua</span>
            </div>
            <div class="space-y-3">
                <div v-for="i in 5" :key="i"
                    class="flex gap-3 items-start pb-2.5 border-b border-gray-100 last:border-0 last:pb-0">
                    <span class="text-lg font-black text-[#A72185] opacity-30 leading-none">0{{ i }}</span>
                    <div class="space-y-0.5">
                        <span class="text-[9px] text-[#A72185] font-bold uppercase">Pemerintahan</span>
                        <h4
                            class="text-xs font-bold text-gray-800 leading-snug line-clamp-2 hover:text-[#A72185] cursor-pointer transition">
                            Bupati Resmikan Jembatan Cirahong Sebagai Kawasan Akses Wisata Baru
                        </h4>
                        <span class="text-[9px] text-gray-400 block">1.4k dibaca</span>
                    </div>
                </div>
            </div>
        </div>

        <!-- Tag Popular -->
        <div class="bg-white rounded p-3 border border-gray-200 shadow-xs">
            <h3 class="text-xs font-bold text-gray-900 mb-2.5 flex items-center gap-1">
                <svg class="w-3.5 h-3.5 text-[#A72185]" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                        d="M7 20l4-16m2 16l4-16M6 9h14M4 15h14" />
                </svg>
                Fokus Isu & Tag Populer
            </h3>
            <div class="flex flex-wrap gap-1.5">
                <span
                    v-for="tag in ['#AlunAlunCiamis', '#WisataGaluh', '#KulinerCiamis', '#PSGCCiamis', '#PendidikanCiamis']"
                    :key="tag"
                    class="bg-gray-100 hover:bg-[#A72185] hover:text-white text-gray-600 text-[10px] px-2 py-1 rounded cursor-pointer transition">
                    {{ tag }}
                </span>
            </div>
        </div>

        <!-- Official Redaksi Banner -->
        <div class="bg-[#A72185] text-white p-3.5 rounded shadow-xs text-center space-y-2">
            <h4 class="text-xs font-bold">Kanal Pengaduan Lapor!</h4>
            <p class="text-[10px] text-pink-100 leading-relaxed">
                Punya keluhan seputar fasilitas publik atau layanan di Ciamis? Kirimkan langsung ke redaksi.
            </p>
            <button
                class="bg-white text-[#A72185] font-bold text-[11px] px-3 py-1.5 rounded hover:bg-gray-100 transition inline-flex items-center gap-1.5 cursor-pointer shadow-xs">
                <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 12 12">
                    <path d="M0 0h12v12H0z" fill="none" />
                    <path fill="#a72185"
                        d="M5.561 2.551a.84.84 0 0 0-1.033-.514c-.973.3-1.653 1.135-1.507 2.101A8.7 8.7 0 0 0 4.092 7.18a8.8 8.8 0 0 0 2.083 2.445c.754.61 1.812.442 2.558-.258A.85.85 0 0 0 8.81 8.21l-.534-.653a.845.845 0 0 0-.91-.272l-1.232.39l-.215-.222a5 5 0 0 1-.706-.929a4.8 4.8 0 0 1-.446-1.079l-.083-.295l.95-.875a.86.86 0 0 0 .221-.935zm-1.327-1.47a1.84 1.84 0 0 1 2.264 1.121l.293.788a1.86 1.86 0 0 1-.48 2.019l-.49.451c.063.174.148.373.258.566c.11.19.238.363.355.504l.63-.2a1.845 1.845 0 0 1 1.985.593l.534.653a1.85 1.85 0 0 1-.166 2.52c-.994.933-2.617 1.32-3.87.306a9.8 9.8 0 0 1-2.32-2.722a9.7 9.7 0 0 1-1.195-3.393c-.24-1.593.903-2.806 2.202-3.205" />
                </svg>
                Panggil Darurat 112
            </button>
        </div>
    </aside>
</template>