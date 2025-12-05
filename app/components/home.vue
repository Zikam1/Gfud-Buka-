<template>
  <div class="bg-gray-50 text-gray-900 font-sans">
    <section 
      class="relative h-[85vh] flex flex-col lg:flex-row items-center justify-center px-4 sm:px-10 bg-cover bg-center bg-no-repeat"
      style="background-image: url('/assest/plll.jpeg');"
    >
   
      <div class="absolute inset-0 bg-black/50 z-0"></div>
      <div class="relative z-10 w-full lg:w-[55%] flex flex-col items-center lg:items-start px-4 lg:px-24  text-center lg:text-left">
        <h1 class="text-2xl sm:text-3xl md:text-4xl lg:text-5xl font-bold text-white leading-snug lg:leading-tight">
          <span class="text-red-500">A</span> WORLD OF FLAVOUR  
          <span class="text-red-500">IN EVERY DISH</span>
        </h1>

        <p class="mt-4 text-gray-300 text-lg sm:text-xl md:text-2xl">
          COOKED WITH LOVE.
        </p>

        <div class="mt-6 flex flex-col sm:flex-row gap-4 w-full sm:w-[80%] justify-center lg:justify-start">
          <div class="bg-red-500/80 backdrop-blur-md p-3 sm:p-4 rounded-xl flex flex-col items-center w-full sm:w-1/2">
            <p class="text-white text-center font-semibold text-sm sm:text-base">
              Delicious Taste
            </p>
          </div>

          <div class="bg-white/20 backdrop-blur-md p-3 sm:p-4 rounded-xl flex flex-col items-center w-full sm:w-1/2">
            <p class="text-white text-center font-semibold text-sm sm:text-base">
              Fresh Ingredients
            </p>
          </div>
        </div>
      </div>

      <div class="relative z-10 w-full lg:w-[45%] flex justify-center mt-8 lg:mt-0">
        <img 
          src="/assest/fggh.png" 
          alt="ingredients image"
          class="w-[180px] sm:w-[220px] md:w-[280px] lg:w-[350px] xl:w-[380px] object-contain drop-shadow-2xl"
        />
      </div>
    </section>
  </div>
</template>
