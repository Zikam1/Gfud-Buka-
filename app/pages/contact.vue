<template>
<section class="relative overflow-hidden bg-gradient-to-b from-[#fff3f0] via-white to-[#fffde6] pt-36">

  <!-- Soft floating circles -->
  <div class="absolute -top-10 -left-10 w-64 h-64 bg-red-200/30 rounded-full blur-3xl"></div>
  <div class="absolute -bottom-20 -right-20 w-72 h-72 bg-yellow-200/30 rounded-full blur-3xl"></div>

  <!-- HERO -->
  <div class="max-w-5xl mx-auto text-center px-6">
    <h1 class="text-4xl sm:4text-xl font-extrabold text-gray-900 drop-shadow-lg leading-tight">
      Contact Gfud <span class="text-yellow-600">— Good Food, Anytime</span>
    </h1>
    <p class="mt-6 text-lg sm:text-xl text-gray-700 max-w-3xl mx-auto leading-relaxed">
      Stop by or call any of our locations. Every Gfud restaurant is ready to welcome you with warmth, flavour, and joy.
    </p>
    <div class="mx-auto w-32 h-1 rounded-full bg-gradient-to-r from-yellow-400 via-yellow-500 to-red-300 mt-8"></div>
  </div>

  <!-- Wavy transition -->
  <div class="mt-24">
    <svg class="w-full" viewBox="0 0 1440 150" preserveAspectRatio="none">
      <path fill="white" d="M0,96L1440,0L1440,160L0,160Z"></path>
    </svg>
  </div>

  <!-- LOCATIONS -->
  <div class="relative bg-white py-32">
    <div class="max-w-6xl mx-auto px-6 space-y-32">

      <!-- Location 1 -->
      <div class="flex flex-col lg:flex-row items-center gap-16">
        <div class="relative lg:w-1/2">
          <div class="absolute -top-8 -left-8 w-56 h-56 bg-red-200/30 rounded-full blur-2xl"></div>
          <img src="/assest/loc.png" 
               class="relative rounded-3xl shadow-2xl w-full object-cover lg:h-96 border-[6px] border-white"/>
        </div>
        <div class="lg:w-1/2 text-center xl:text-left">
          <h2 class="text-3xl font-extrabold text-red-600/90">Gfud – Agege, Lagos</h2>
          <p class="mt-4 text-gray-600 text-lg">37, Dopemu Road Apapa Ashafa Bus Stop .</p>
          <p class="mt-2 font-semibold text-gray-800 text-lg">Tel: +234 815 922 4126</p>
        </div>
      </div>

      <!-- Location 2 -->
      <div class="flex flex-col lg:flex-row-reverse items-center gap-16">
        <div class="relative lg:w-1/2">
          <div class="absolute -top-10 -right-10 w-60 h-60 bg-yellow-200/30 rounded-full blur-2xl"></div>
          <!-- <img src="/assest/friedrice.jpg" 
               class="relative rounded-3xl shadow-2xl w-full object-cover lg:h-96 border-[6px] border-white"/> -->
        </div>
        <div class="lg:w-1/2 text-center lg:text-left">
          <h2 class="text-4xl font-extrabold text-yellow-600/90">Gfud Ijaiye– Lagos State</h2>
          <p class="mt-4 text-gray-600 text-lg">76 Agbado Ijaiye road Jankara.</p>
          <p class="mt-2 font-semibold text-gray-800 text-lg">Tel: +234 808 963 8661</p>
        </div>
      </div>

      <!-- Location 3 -->
      <div class="flex flex-col lg:flex-row items-center gap-16">
        <div class="relative lg:w-1/2">
          <div class="absolute -top-6 -left-6 w-56 h-56 bg-red-200/30 rounded-full blur-2xl"></div>
          <!-- <img src="/assest/chicken.jpg" 
               class="relative rounded-3xl shadow-2xl w-full object-cover lg:h-96 border-[6px] border-white"/> -->
        </div>
        <div class="lg:w-1/2 text-center lg:text-left">
          <h2 class="text-4xl font-extrabold text-red-600/90">Gfud – Lagos, coming soon....</h2>
          <p class="mt-4 text-gray-600 text-lg">Otunbu</p>
          <p class="mt-2 font-semibold text-gray-800 text-lg">Tel: +234 701 998 2211</p>
        </div>
      </div>

    </div>
  </div>

  <!-- SOCIALS -->
  <div class="bg-gradient-to-b from-white to-[#fffbe9] py-20 text-center">
    <h3 class="text-3xl font-bold text-gray-900">Connect With Gfud</h3>
    <p class="mt-3 text-gray-600 max-w-xl mx-auto">Follow us for exclusive updates, promos, and mouth-watering dishes.</p>

    <div class="flex justify-center gap-8 mt-6 text-3xl">
      <a href="#" class="hover:scale-110 transition text-red-600/90">📘</a>
      <a href="#" class="hover:scale-110 transition text-red-600/90">📸</a>
      <a href="#" class="hover:scale-110 transition text-red-600/90">🎵</a>
    </div>
  </div>

</section>
</template>

<script setup>
</script>