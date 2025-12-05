<template>
  <section 
    class="relative py-24 bg-cover bg-center bg-no-repeat"
    style="background-image: url('/assest/subscribe-bg.jpg');"
  >
    <!-- Darker overlay -->
    <div class="absolute inset-0 bg-black/90"></div>

    <div class="relative max-w-4xl mx-auto px-6 text-center text-white">
      
      <!-- Main Heading -->
      <h2 class="text-3xl md:text-4xl font-bold mb-4">
        Subscribe for More
      </h2>
      
      <!-- Subheading -->
      <p class="text-xl md:text-xl mb-8 text-gray-200">
        Get the latest updates, special offers, and delicious news from 
        <span class="font-semibold text-yellow-400">GFud</span>.
      </p>

      <!-- Subscription box -->
      <div 
        class="bg-white/10 backdrop-blur-md rounded-2xl p-6 md:p-10 
               flex flex-col md:flex-row items-center justify-center 
               gap-4 shadow-xl border border-white/20"
      >
        
        <!-- Input -->
        <input 
          type="email" 
          placeholder="Enter your email" 
          class="w-full md:w-2/3 px-4 py-3 rounded-lg text-gray-900 
                 placeholder-gray-500 focus:outline-none focus:ring-2 
                 focus:ring-yellow-400"
        />

        <!-- Subscribe button -->
        <button 
          class="px-6 py-3 bg-yellow-500 text-gray-900 font-semibold 
                 rounded-lg shadow hover:bg-yellow-600 transition"
        >
          Subscribe
        </button>

      </div>

      <!-- Optional small text -->
      <p class="mt-4 text-gray-300 text-sm">
        No spam, unsubscribe anytime.
      </p>

    </div>
  </section>
</template>