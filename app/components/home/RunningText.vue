<template>
    <div
        class="bg-white border border-pink-200 rounded p-3 flex flex-col md:flex-row md:items-center justify-between gap-4 shadow-xs font-sans">
        <div class="flex items-center gap-3.5 overflow-hidden">

            <!-- Detail Teks -->
            <div class="min-w-0">
                <h3 class="font-bold text-gray-900 text-sm leading-snug">
                    Kanal Transparansi & Data Statistik Ciamis 2026
                </h3>
                <p class="text-xs text-gray-500 font-normal truncate mt-0.5">
                    Pantau capaian inflasi daerah, realisasi APBD Kab. Ciamis, dan indeks pelayanan kepuasan publik
                    secara berkala.
                </p>
            </div>
        </div>

        <!-- Sisi Kanan: Tombol Aksi -->
        <div class="flex items-center gap-2.5 flex-shrink-0">
            <button
                class="bg-[#A72185] text-white font-semibold px-4 py-2 rounded-lg text-xs hover:bg-[#8e1b70] transition flex items-center gap-1.5 shadow-xs">
                Lihat Dasbor APBD
                <svg class="w-3.5 h-3.5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                        d="M10 6H6a2 2 0 00-2 2v10a2 2 0 002 2h10a2 2 0 002-2v-4M14 4h6m0 0v6m0-6L10 14" />
                </svg>
            </button>

            <button
                class="bg-gray-100 text-gray-800 font-semibold px-4 py-2 rounded-lg text-xs hover:bg-gray-200 transition border border-gray-200">
                Portal PPID Ciamis
            </button>
        </div>
    </div>
</template>