<template>
    <div class="min-h-screen bg-gray-50 flex flex-col font-sans text-gray-800">
        <!-- Header & Navigasi -->
        <Navbar />

        <main class="flex-1 max-w-7xl w-full mx-auto px-4 py-6">
            <slot />
        </main>

        <!-- Footer -->
        <Footer />
    </div>
</template>

<script setup>
import Navbar from '~/components/Navbar.vue'
import Footer from '~/components/Footer.vue'
</script>