<template>
<section class="bg-gradient-to-b from-red-50 via-white to-yellow-50 text-gray-900">

  <!-- HERO -->
  <div class="max-w-7xl mx-auto px-6 py-20 lg:py-28">
    <div class="grid grid-cols-1 lg:grid-cols-2 gap-14 items-center">

      <!-- TEXT -->
      <div>
        <p class="inline-block px-4 py-1 bg-red-600/10 text-red-700 rounded-full text-sm font-semibold mb-5">
          About Gfud
        </p>

        <h1 class="text-3xl sm:text-3xl xl:text-4xl font-extrabold leading-tight tracking-tight text-gray-900">
          Gfud — Good Food for Every Moment
        </h1>

        <p class="mt-6 text-lg text-gray-700 max-w-xl">
          At <span class="font-semibold text-red-600">Gfud</span>, we create meals that bring people together.
          Every dish is crafted with passion — rich colours, bold flavours, and the kind of warmth that makes
          food feel like home. Our red and yellow brand palette mirrors what we stand for: passion, flavour,
          and sunshine in every bite.
        </p>

        <div class="mt-10 flex flex-wrap gap-4">
          <NuxtLink
            to="/menu"
            class="inline-flex items-center gap-2 px-6 py-3 bg-red-600 hover:bg-red-700 text-white rounded-xl shadow-md font-medium transition-all"
          >
            Explore Our Menu
          </NuxtLink>

          <NuxtLink
            to="/reservations"
            class="inline-flex items-center gap-2 px-6 py-3 border-2 border-red-600 text-red-600 hover:bg-red-50 rounded-xl font-medium transition-all"
          >
            Book a Table
          </NuxtLink>
        </div>
      </div>

      <div class="relative h-full flex justify-center">
        <div class="rounded-3xl overflow-hidden shadow-xl w-80 h-80 object-cover">
          <img src="/assest/chc.png" alt="Food plating" class="w-full h-full object-cover"/>
        </div>

        <div class="absolute -bottom-10 -right-10 w-52 h-52 rounded-2xl overflow-hidden shadow-2xl border-4 border-white">
          <img src="/assest/uuu.jpg" alt="Dish close-up" class="w-full h-full object-cover"/>
        </div>
      </div>

    </div>
  </div>

  <!-- MISSION + VISION + VALUES -->
  <div class="max-w-7xl mx-auto px-6 pb-20">
    <div class="grid grid-cols-1 md:grid-cols-3 gap-8">

      <!-- Mission -->
      <article class="bg-white p-8 rounded-3xl shadow-sm border border-red-100 hover:shadow-lg transition-all">
        <h3 class="text-2xl font-bold text-red-600">Our Mission</h3>
        <p class="mt-4 text-gray-700 leading-relaxed">
          To serve fresh, flavour-rich meals that turn everyday moments into memorable experiences — simple,
          honest, and always crafted with care.
        </p>
      </article>

      <!-- Vision -->
      <article class="bg-white p-8 rounded-3xl shadow-sm border border-yellow-100 hover:shadow-lg transition-all">
        <h3 class="text-2xl font-bold text-yellow-600">Our Vision</h3>
        <p class="mt-4 text-gray-700 leading-relaxed">
          To be the go-to food destination that brings communities together — locally rooted, globally inspired,
          and forever welcoming.
        </p>
      </article>

      <!-- Values -->
      <article class="bg-white p-8 rounded-3xl shadow-sm border border-red-100 hover:shadow-lg transition-all">
        <h3 class="text-2xl font-bold text-red-600">Our Values</h3>
        <ul class="mt-4 text-gray-700 space-y-2">
          <li class="flex items-center gap-2"><span class="text-red-500">•</span> Fresh ingredients</li>
          <li class="flex items-center gap-2"><span class="text-red-500">•</span> Bold flavours</li>
          <li class="flex items-center gap-2"><span class="text-red-500">•</span> Community-first mindset</li>
          <li class="flex items-center gap-2"><span class="text-red-500">•</span> Sustainability & minimal waste</li>
        </ul>
      </article>

    </div>
  </div>

</section>
</template>

<script setup>
</script>