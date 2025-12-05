<template>
  <div>

    <!-- WHITE FOOTER SECTION -->
    <div class="bg-white text-gray-700 py-16 border-t border-gray-200">
      <div class="max-w-7xl mx-auto px-6 grid grid-cols-1 md:grid-cols-3 gap-12">

        <!-- LEFT SECTION -->
        <div>
          <h2 class="text-3xl font-bold text-gray-900">GFud</h2>
          <p class="mt-3 text-gray-600 text-sm leading-relaxed">
            Good food made with love, bringing you the best meals with authentic taste.
          </p>
        </div>

        <!-- MIDDLE SECTION (NOW USING NuxtLink) -->
        <div class="text-left sm:text-left">
          <h3 class="text-xl font-semibold text-gray-900 mb-3">Restaurant</h3>
          <ul class="space-y-2 text-gray-600 text-sm">
            <li>
              <NuxtLink to="/about" class="hover:text-yellow-500 transition">
                About
              </NuxtLink>
            </li>

            <li>
              <NuxtLink to="/menu" class="hover:text-yellow-500 transition">
                Menu
              </NuxtLink>
            </li>

            <li>
              <NuxtLink to="/contact" class="hover:text-yellow-500 transition">
                Contact
              </NuxtLink>
            </li>
          </ul>
        </div>

        <!-- RIGHT SECTION - NEWSLETTER -->
        <div>
          <h3 class="text-xl font-semibold text-gray-900 mb-3">Newsletter</h3>

          <!-- FORM INPUT -->
          <div class="flex items-center bg-gray-100 rounded-lg overflow-hidden shadow-sm">
            <input 
              type="email"
              placeholder="Enter your email"
              class="w-full px-4 py-3 bg-transparent text-gray-700 placeholder-gray-500 focus:outline-none"
            />
            <button class="px-4 py-3 bg-yellow-500 text-gray-900 font-semibold hover:bg-yellow-600 transition">
              Join
            </button>
          </div>

          <p class="text-gray-600 text-xs mt-3">
            Stay updated with our latest meals and special offers.
          </p>
        </div>

      </div>

      <!-- BOTTOM LINE -->
      <div class="text-center mt-16 text-gray-500 text-sm">
        © 2025 GFud — All Rights Reserved.
      </div>
    </div>

    <!-- BLACK BAR AFTER FOOTER -->
    <div class="bg-black w-full py-12">
      <div class="max-w-7xl mx-auto px-6">
        <p class="text-gray-400 text-sm">
          Privacy Policy / GFud 2025
        </p>
      </div>
    </div>

  </div>
</template>

<script setup>
// No script needed
</script>