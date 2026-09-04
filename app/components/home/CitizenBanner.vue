<template>
    <div class="bg-slate-100/80 border border-slate-200/80 rounded p-3 md:p-6 relative overflow-hidden shadow-xs">
        <!-- <div class="absolute right-1 bottom-1 opacity-15 grayscale pointer-events-none select-none">
            <img src="/logo-ciamis.png" alt="Logo Kabupaten Ciamis" class="w-34 h-34 object-contain" />
        </div> -->

        <div class="relative z-10 flex flex-col lg:flex-row lg:items-center justify-between gap-5">
            <!-- Teks Informasi Kiri -->
            <div class="max-w-3xl space-y-1.5">
                <div class="flex items-center gap-2">
                    <span class="w-2 h-2 rounded-full bg-[#A72185] animate-pulse"></span>
                    <span class="text-[10px] font-extrabold uppercase tracking-widest text-[#A72185]">
                        Jurnalisme Warga Tatar Galuh
                    </span>
                </div>
                <h3 class="text-base sm:text-lg md:text-xl font-bold text-gray-900 leading-snug">
                    Punya Informasi Seputar Desa atau Komunitas Anda di Ciamis?
                </h3>
                <p class="text-xs text-gray-600 leading-relaxed">
                    Kirimkan siaran pers kegiatan, opini santri, liputan budaya kampung, atau informasi penting lainnya
                    ke meja redaksi Ciamis News untuk dipublikasikan setelah dikurasi.
                </p>
            </div>

            <!-- Aksi Kanan -->
            <div class="flex flex-col sm:flex-row items-stretch sm:items-center gap-2.5 flex-shrink-0">
                <a href="https://wa.me/628123456789" target="_blank"
                    class="bg-[#A72185] hover:bg-[#8e1b70] text-white font-bold text-xs px-4 py-2.5 rounded-lg flex items-center justify-center gap-2 transition shadow-xs cursor-pointer">
                    <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24">
                        <path d="M0 0h24v24H0z" fill="none" />
                        <path fill="none" stroke="#fff" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                            d="M3.714 3.048a.498.498 0 0 0-.683.627l2.843 7.627a2 2 0 0 1 0 1.396l-2.842 7.627a.498.498 0 0 0 .682.627l18-8.5a.5.5 0 0 0 0-.904zM6 12h16" />
                    </svg>
                    Kirim Liputan Warga
                </a>

                <a href="#"
                    class="bg-white hover:bg-gray-50 border border-gray-200 text-gray-700 font-semibold text-xs px-3.5 py-2.5 rounded-lg flex items-center justify-center gap-1.5 transition cursor-pointer">
                    Panduan Kurasi
                </a>
            </div>
        </div>
    </div>
</template>