<template>
  <div>

    <!-- ================= FOOD MENU ================= -->
    <section class="py-20 bg-gray-100">
      <div class="max-w-7xl mx-auto px-6 text-center">

        <!-- MAIN HEADING -->
        <h2 class="text-3xl font-bold text-gray-900">Our Food Menu</h2>
        <p class="text-gray-600 mt-2 text-lg">
          <span class="font-semibold">GFud</span> – Good Food
        </p>

        <!-- GRID -->
        <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-10 mt-14">

          <!-- FOOD CARD -->
          <div
            v-for="food in foods"
            :key="food.id"
            class="bg-white rounded-2xl shadow-xl overflow-hidden hover:shadow-2xl transition duration-300 flex flex-col justify-between"
          >

            <!-- IMAGE WRAPPER -->
            <div class="flex justify-center p-4">
              <img
                :src="food.image"
                alt="Food Image"
                class="h-32 w-auto object-cover rounded-lg"
              />
            </div>

            <!-- TEXT -->
            <div class="p-6 flex-1 flex flex-col justify-between">

              <div>
                <h3 class="text-yellow-500 font-bold text-lg">
                  {{ food.name }}
                </h3>

                <p class="text-gray-600 text-sm mt-1 leading-relaxed">
                  {{ food.desc }}
                </p>
              </div>

              <!-- LINE DIVIDER -->
              <div class="mt-5 mb-4">
                <div class="h-px bg-gray-200 w-full"></div>
              </div>

              <!-- RESERVE + PRICE -->
              <div class="flex items-center justify-between">

                <!-- RESERVE MEAL BUTTON -->
                <NuxtLink
                  :to="`/menu`"
                  class="px-3 py-1 bg-red-600 text-white text-sm rounded-lg font-semibold shadow hover:bg-red-700 transition"
                >
                  Reserve Meal
                </NuxtLink>

                <!-- PRICE -->
                <span class="font-bold text-gray-900 text-lg">
                  ₦{{ (food.unitPrice * food.quantity).toLocaleString() }} {{ food.unitText }}
                </span>

              </div>

            </div>
          </div>

        </div>
      </div>
    </section>

    <!-- ================= TESTIMONIALS ================= -->
    <section class="py-20 bg-gray-50">
  <div class="max-w-7xl mx-auto px-6 text-center">
    <h2 class="text-3xl font-bold text-gray-900">Testimonials</h2>
    <p class="text-gray-600 mt-2 text-lg">What Our Customers Say</p>

    <div class="mt-12 flex flex-wrap justify-center gap-8">
      <div
        v-for="customer in customers"
        :key="customer.id"
        class="flex flex-col items-center max-w-xs"
      >
        <!-- Use customer-specific image -->
        <img
          :src="customer.image"
          alt="Customer"
          class="w-32 h-32 rounded-full object-cover object-center border-4 border-yellow-500 shadow-lg"
        />

        <div class="mt-4 bg-white p-6 rounded-2xl shadow-xl text-left relative w-full">
          <div class="flex items-center justify-between mb-1">
            <h3 class="text-gray-900 font-bold">{{ customer.name }}</h3>
            <div class="flex space-x-1">
              <svg v-for="i in 5" :key="i" class="w-4 h-4 text-yellow-400" fill="currentColor" viewBox="0 0 20 20">
                <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.176 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118L2.98 8.719c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z"/>
              </svg>
            </div>
          </div>

          <span class="text-gray-500 text-xs">{{ customer.position }}</span>
          <p class="text-gray-700 text-sm leading-relaxed mb-4">
            "{{ customer.testimonial }}"
          </p>

          <div class="absolute -top-4 left-1/2 -translate-x-1/2 w-0 h-0 
                      border-l-transparent border-r-transparent border-b-white 
                      border-l-6 border-r-6 border-b-6"></div>
        </div>
      </div>
    </div>
  </div>
</section>

  </div>
</template>

<script setup>
import { reactive } from "vue";

const foods = reactive([
  { id: 1, name: "Jollof Rice", desc: "Smoky party-style jollof cooked with rich spices.", unitPrice: 500, unitText: "per portion", quantity: 1, image: "/assest/jolof.png" },
  { id: 2, name: "Grilled Turkey", desc: "Charcoal-grilled, juicy and perfectly seasoned.", unitPrice: 3500, unitText: "", quantity: 1, image: "/assest/grill.png" },
  { id: 3, name: "Shawarma", desc: "Creamy, spicy and fully loaded with goodness.", unitPrice: 4000, unitText: "", quantity: 1, image: "/assest/shaar.png" },
  { id: 4, name: "Eba & Egusi", desc: "Delicious traditional meal.", unitPrice: 2500, unitText: "", quantity: 1, image: "/assest/ebe-egusi.png" },
  { id: 5, name: "Fried Rice", desc: "Delicious and colorful fried rice.", unitPrice: 500, unitText: "per portion", quantity: 1, image: "/assest/fried.png" },
  { id: 6, name: "Meat-pie", desc: "Hot, fresh, and extra cheesy.", unitPrice: 800, unitText: "", quantity: 1, image: "/assest/meat.png" }
]);

const customers = [
  {
    id: 1,
    name: 'Adiele Favour',
    position: 'CEO, TechCorp',
    testimonial: 'Fantastic!!! Highly recommended for anyone looking for quality.',
    image: '/assest/mann.png'
  },
  {
    id: 2,
    name: 'Chioma Okeke',
    position: 'Marketing Head, BizGrow',
    testimonial: 'Amazing experience, customer support is top-notch and very responsive.',
    image: '/assest/mannn.png'
  },
  {
    id: 3,
    name: 'Usman Musa',
    position: 'Freelancer',
    testimonial: 'Truly transformed my workflow. Efficiency has doubled since using this.',
    image: '/assest/man.png'
  }

];
</script>