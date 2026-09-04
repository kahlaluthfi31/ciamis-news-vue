<template>
    <div class="space-y-8">
        <!-- 1. Hero Section (Berita Utama & Berita Pilihan) -->
        <HeroSection />

        <!-- 2. Running Text / Info Banner -->
        <RunningText />

        <!-- Section 3: Main Grid (items-start wajib agar sticky bekerja) -->
        <div class="grid grid-cols-1 lg:grid-cols-12 gap-6 items-start">
            <!-- Kolom Kiri: Berita Terkini (8 Kolom) -->
            <div class="lg:col-span-8">
                <NewsGrid />
            </div>
            <!-- Kolom Kanan: Sidebar Sticky (4 Kolom) -->
            <aside class="lg:col-span-4 sticky top-6 space-y-5">
                <SidebarWidget />
            </aside>
        </div>

        <!-- 4. Citizen Report Banner -->
        <CitizenBanner />
    </div>
</template>

<script setup>
import HeroSection from '~/components/home/HeroSection.vue'
import RunningText from '~/components/home/RunningText.vue'
import NewsGrid from '~/components/home/NewsGrid.vue'
import SidebarWidget from '~/components/home/SidebarWidget.vue'
import CitizenBanner from '~/components/home/CitizenBanner.vue'
</script>