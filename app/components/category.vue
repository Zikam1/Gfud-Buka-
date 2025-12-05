<template>
  <!-- ====================================== -->
  <!--           CATEGORY SECTION            -->
  <!-- ====================================== -->
  <section class="py-14 sm:py-16 bg-gray-50">
    <!-- Header -->
    <div class="text-center max-w-2xl mx-auto px-4 mb-8">
      <p class="text-xs sm:text-sm uppercase text-gray-400 mb-2 tracking-wide">{{ category }}</p>
      <h2 class="text-2xl sm:text-3xl font-bold text-gray-900 mb-2">{{ title }}</h2>
      <p class="text-yellow-500 font-medium mb-4">Gfud, Good Food</p>
      <div class="w-14 sm:w-16 h-1 bg-yellow-500 rounded-full mx-auto"></div>
    </div>

    <!-- Scrollable boxes -->
    <div class="px-4 sm:px-6 overflow-x-auto">
      <div class="flex gap-4 mx-auto w-max">
        <div
          v-for="item in items"
          :key="item.title"
          class="w-28 sm:w-32 h-36 sm:h-40 bg-white rounded-xl shadow text-center p-2 
                 flex-shrink-0 hover:scale-105 transform transition"
        >
          <img :src="item.img" alt="" class="h-16 sm:h-20 w-full object-cover rounded-lg mb-2" />
          <h3 class="text-xs sm:text-sm font-semibold text-gray-900">{{ item.title }}</h3>
          <p class="text-[10px] sm:text-xs text-yellow-500">{{ item.subtitle }}</p>
        </div>
      </div>
    </div>
  </section>


  <!-- ====================================== -->
  <!--           ABOUT US SECTION             -->
  <!-- ====================================== -->
  <section class="py-16 bg-white">
    <div class="max-w-6xl mx-auto px-4 sm:px-6 grid grid-cols-1 md:grid-cols-2 gap-10 items-center">

      <!-- Left Image -->
      <div class="w-full">
        <img 
          src="/assest/sp.jpeg"
          alt="Food Display"
          class="rounded-2xl shadow-lg w-full md:h-80 object-cover"
        />
      </div>

      <!-- Right Text -->
      <div>
        <p class="text-yellow-500 uppercase tracking-wide text-sm mb-2">
          About Us
        </p>

        <h2 class="text-2xl sm:text-3xl font-bold text-gray-900 mb-4 leading-snug">
          Cooked with Love, served with every pride of 
          <span class="text-yellow-500">flavor in every dish</span>
        </h2>

        <p class="text-gray-600 leading-relaxed mb-4 text-sm sm:text-base">
          At GFUD, we prepare every meal with the finest ingredients to ensure freshness, quality, 
          and exceptional taste remain at the heart of every serving.
        </p>

        <div class="bg-yellow-100 border-l-4 border-yellow-500 p-4 rounded-lg mb-6">
          <p class="text-gray-800 font-medium text-sm sm:text-base">
            "Good food is more than a meal — it's an experience we take pride in delivering."
          </p>
        </div>
      </div>

    </div>
  </section>


  <!-- ====================================== -->
  <!--         WHY CHOOSE US SECTION          -->
  <!-- ====================================== -->
  <section 
    class="relative py-20 sm:py-28 bg-cover bg-center bg-no-repeat"
    style="background-image: url('/assest/black-bg.jpg');"
  >
    <div class="absolute inset-0 bg-black/85"></div>

    <div class="relative max-w-6xl mx-auto px-4 sm:px-6 text-center">

      <div class="mb-10 sm:mb-12">
        <p class="text-yellow-500 uppercase tracking-wide text-sm mb-2">Why Choose Us</p>
        <h2 class="text-2xl sm:text-3xl font-bold text-white">
          Experience the Best of Quality & Taste
        </h2>
      </div>
      
      <!-- Icons -->
      <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6">

        <!-- Box 1 -->
        <div class="bg-white/10 backdrop-blur-md rounded-xl p-6 text-center shadow-lg border border-white/10">
          <div class="w-12 h-12 mx-auto mb-3 rounded-full bg-yellow-500 flex items-center justify-center">
            <div class="w-3 h-3 bg-white rounded-full"></div>
          </div>
          <h3 class="text-white font-bold text-lg">Quality Meals</h3>
          <p class="text-gray-300 text-sm mt-1">Fresh ingredients cooked to perfection.</p>
        </div>

        <!-- Box 2 -->
        <div class="bg-white/10 backdrop-blur-md rounded-xl p-6 text-center shadow-lg border border-white/10">
          <div class="w-12 h-12 mx-auto mb-3 rounded-full bg-yellow-500 flex items-center justify-center">
            <div class="w-0 h-0 
              border-l-4 border-r-4 border-b-8 
              border-l-transparent border-r-transparent 
              border-b-white"
            ></div>
          </div>
          <h3 class="text-white font-bold text-lg">Fast Delivery</h3>
          <p class="text-gray-300 text-sm mt-1">Your order arrives quickly and hot.</p>
        </div>

        <!-- Box 3 -->
        <div class="bg-white/10 backdrop-blur-md rounded-xl p-6 text-center shadow-lg border border-white/10">
          <div class="w-12 h-12 mx-auto mb-3 rounded-full bg-yellow-500 flex items-center justify-center relative">
            <div class="w-3 h-3 bg-white rounded-full absolute top-1 left-2 rotate-45"></div>
            <div class="w-3 h-3 bg-white rounded-full absolute top-1 right-2 rotate-45"></div>
            <div class="w-3 h-3 bg-white absolute top-3 left-1/2 -translate-x-1/2 rotate-45"></div>
          </div>
          <h3 class="text-white font-bold text-lg">Made With Love</h3>
          <p class="text-gray-300 text-sm mt-1">Every dish crafted with passion.</p>
        </div>

      </div>
    </div>
  </section>
</template>

<script setup>
const props = defineProps({
  category: { type: String, default: 'CATEGORY' },
  title: { type: String, default: 'Delicious Treats' }
})

const items = [
  { title: 'Cake', subtitle: 'Baked', img: '/assest/cck.png' },
  { title: 'Ice Cream', subtitle: 'Served', img: '/assest/ck.png' },
  { title: 'Cupcake', subtitle: 'Baked', img: '/assest/cup-ca.png' },
  { title: 'Donut', subtitle: 'Soft', img: '/assest/Donut.png' },
  { title: 'Parfait', subtitle: 'Healthy', img: '/assest/parf.png' },
]
</script>
