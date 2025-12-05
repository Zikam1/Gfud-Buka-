<template>
  <nav class="w-full bg-white/95 backdrop-blur-md shadow-md fixed top-0 left-0 z-50">
    <div class="max-w-7xl container mx-auto px-6 py-4 flex justify-between items-center">

      <!-- LOGO - Centered & Classy -->
      <NuxtLink to="/" class="flex items-center space-x-2">
        <img
          src="/assest/GfudB.jpg"
          alt="Restaurant Logo"
          class="h-16 w-auto object-contain rounded-md shadow-sm hover:scale-105 transition-transform duration-300"
        />
      </NuxtLink>

      <!-- Desktop Navigation -->
      <div class="hidden md:flex items-center space-x-10 font-semibold text-gray-700">
        <NuxtLink to="/" class="hover:text-red-500 transition">Home</NuxtLink>

        <NuxtLink to="/about" class="hover:text-red-500 transition">About</NuxtLink>
        <NuxtLink to="/contact" class="hover:text-red-500 transition">Contact</NuxtLink>

     
        <NuxtLink
          to="/menu"
          class="bg-red-500 text-white px-5 py-2 rounded-full shadow-md hover:bg-red-600 transition"
        >
          Menu
        </NuxtLink>
      </div>

   
      <button
        @click="isOpen = !isOpen"
        class="md:hidden text-3xl text-gray-800 focus:outline-none"
      >
        <span v-if="!isOpen">☰</span>
        <span v-else>✕</span>
      </button>
    </div>

    <!-- Mobile Menu -->
    <transition name="slide">
      <div v-if="isOpen" class="md:hidden bg-white shadow-lg border-t py-6">
        <div class="flex flex-col items-center space-y-6 font-semibold text-gray-700">

          <NuxtLink to="/" class="hover:text-red-500" @click="isOpen = false">Home</NuxtLink>
          <NuxtLink to="/about" class="hover:text-red-500" @click="isOpen = false">About</NuxtLink>
          <NuxtLink to="/contact" class="hover:text-red-500" @click="isOpen = false">Contact</NuxtLink>

          <!-- Mobile CTA -->
          <NuxtLink
            to="/menu"
            class="bg-red-500 text-white px-6 py-2 rounded-full shadow-md hover:bg-red-600 transition"
            @click="isOpen = false"
          >
            Menu
          </NuxtLink>

          <!-- Hotline -->
          <div class="pt-2 text-center">
            <p class="text-gray-700 font-bold text-sm">For Enquiries, Call</p>
            <a href="tel:08023190606" class="text-red-600 font-semibold">070 4027 1579</a>
          </div>
        </div>
      </div>
    </transition>
  </nav>
</template>

<script setup>
import { ref } from 'vue'
const isOpen = ref(false)
</script>

<style>
.slide-enter-active,
.slide-leave-active {
  transition: all 0.3s ease;
}
.slide-enter-from,
.slide-leave-to {
  opacity: 0;
  transform: translateY(-10px);
}
</style>
