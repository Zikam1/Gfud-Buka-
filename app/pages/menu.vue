<template>
  <div class="relative">

    <!-- ================= MAIN FOOD MENU (WITH QTY & PRICE) ================= -->
    <section class="pt-36 pb-20 bg-gray-100">
      <div class="max-w-7xl mx-auto px-6 text-center">

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

            <!-- IMAGE -->
            <div class="flex justify-center p-4">
              <img
                :src="food.image"
                alt="Food Image"
                class="h-32 w-auto object-cover rounded-lg"
              />
            </div>

            <!-- CONTENT -->
            <div class="p-6 flex-1 flex flex-col justify-between">
              <div>
                <h3 class="text-yellow-500 font-bold text-lg">{{ food.name }}</h3>
                <p class="text-gray-600 text-sm mt-1 leading-relaxed">{{ food.desc }}</p>

                <!-- Quantity -->
                <div class="flex items-center gap-2 mt-3 justify-center">
                  <label class="text-gray-700 text-sm font-semibold">Qty:</label>
                  <input
                    type="number"
                    min="1"
                    v-model.number="food.quantity"
                    class="w-16 px-2 py-1 border rounded text-center text-sm"
                  />
                </div>

                <!-- Location Dropdown -->
                <div class="mt-4">
                  <label class="block text-sm font-semibold text-gray-700 mb-1">Location:</label>
                  <select
                    v-model="food.selectedLocation"
                    class="w-full border px-3 py-2 rounded text-sm"
                  >
                    <option value="agege">GFud – Agege, Lagos</option>
                    <option value="ijaiye">GFud Ijaiye – Lagos</option>
                    <option value="otubu" disabled>GFud Otubu – Coming Soon</option>
                  </select>
                </div>
              </div>

              <!-- Divider -->
              <div class="mt-5 mb-4">
                <div class="h-px bg-gray-200 w-full"></div>
              </div>

              <!-- Order Row -->
              <div class="flex items-center justify-between">
                <a
                  :href="generateWhatsAppLink(food)"
                  target="_blank"
                  class="px-3 py-1 bg-red-600 text-white text-sm rounded-lg font-semibold shadow hover:bg-red-700 transition"
                  :class="{
                    'opacity-40 cursor-not-allowed': !isLocationAvailable(food.selectedLocation)
                  }"
                >
                  Order Now
                </a>

                <span class="font-bold text-gray-900 text-lg">
                  ₦{{ (food.unitPrice * food.quantity).toLocaleString() }}
                </span>
              </div>
            </div>

          </div>
        </div>

      </div>
    </section>

    <!-- ================= NEW 3 CARDS (NO QTY, NO PRICE, WITH LOCATION & ORDER) ================= -->
    <section class="pb-20 bg-gray-100">
      <div class="max-w-7xl mx-auto px-6 text-center">

        <h2 class="text-3xl font-bold text-gray-900">Special Dishes</h2>
        <p class="text-gray-600 mt-2 text-lg">Order these directly</p>

        <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-10 mt-14">

          <div
            v-for="item in displayFoods"
            :key="item.id"
            class="bg-white rounded-2xl shadow-xl p-6 flex flex-col items-center hover:shadow-2xl transition duration-300"
          >
            <!-- IMAGE -->
            <img
              :src="item.image"
              alt="Food Image"
              class="h-32 w-auto rounded-lg mb-4"
            />

            <!-- NAME -->
            <h3 class="text-yellow-500 font-bold text-lg">{{ item.name }}</h3>

            <!-- DESCRIPTION -->
            <p class="text-gray-600 text-sm mt-2 leading-relaxed text-center">
              {{ item.desc }}
            </p>

            <!-- LOCATION SELECT (for these cards) -->
            <div class="w-full mt-4">
              <label class="block text-sm font-semibold text-gray-700 mb-1 text-left">Location:</label>
              <select
                v-model="item.selectedLocation"
                class="w-full border px-3 py-2 rounded text-sm"
              >
                <option value="agege">GFud – Agege, Lagos</option>
                <option value="ijaiye">GFud Ijaiye – Lagos</option>
                <option value="otubu" disabled>GFud Otubu – Coming Soon</option>
              </select>
            </div>

            <!-- ORDER BUTTON (uses selectedLocation) -->
            <a
              :href="generateSimpleWhatsAppLink(item)"
              target="_blank"
              class="mt-4 px-4 py-2 bg-red-600 text-white text-sm rounded-lg font-semibold shadow hover:bg-red-700 transition w-full text-center"
              :class="{ 'opacity-40 cursor-not-allowed': !isLocationAvailable(item.selectedLocation) }"
            >
              Order Now
            </a>
          </div>

        </div>
      </div>
    </section>

  </div>
</template>

<script setup>
import { reactive } from "vue";

// WhatsApp numbers for each branch (null = not available)
const locationNumbers = {
  agege: "2348159224126",
  ijaiye: "2348089638661",
  otubu: null,
};

// helper
const isLocationAvailable = (loc) => {
  return !!locationNumbers[loc];
};

// MAIN FOOD LIST (WITH QTY & PRICE)
const foods = reactive([
  {
    id: 1,
    name: "Jollof Rice",
    desc: "Smoky party-style jollof cooked with rich spices.",
    unitPrice: 500,
    quantity: 1,
    image: "/assest/jolof.png",
    selectedLocation: "agege",
  },
  {
    id: 2,
    name: "Grilled Chicken",
    desc: "Charcoal-grilled, juicy and perfectly seasoned.",
    unitPrice: 3500,
    quantity: 1,
    image: "/assest/grill.png",
    selectedLocation: "agege",
  },
  {
    id: 3,
    name: "Ofada Rice",
    desc: "A flavour-packed Nigerian classic.",
    unitPrice: 500,
    quantity: 1,
    image: "/assest/ofad.png",
    selectedLocation: "agege",
  },
  {
    id: 4,
    name: "Eba & Egusi",
    desc: "Delicious traditional meal.",
    unitPrice: 900,
    quantity: 1,
    image: "/assest/ebe-egusi.png",
    selectedLocation: "agege",
  },
  {
    id: 5,
    name: "Fried Rice",
    desc: "Delicious and colorful fried rice.",
    unitPrice: 500,
    quantity: 1,
    image: "/assest/fried.png",
    selectedLocation: "agege",
  },
  {
    id: 6,
    name: "Meat-pie",
    desc: "Hot, fresh, and extra cheesy.",
    unitPrice: 800,
    quantity: 1,
    image: "/assest/meat.png",
    selectedLocation: "agege",
  },
  {
    id: 7,
    name: "Yam",
    desc: "Delicious traditional meal.",
    unitPrice: 900,
    quantity: 1,
    image: "/assest/yam.png",
    selectedLocation: "agege",
  },
  {
    id: 8,
    name: "Plaintain",
    desc: "Delicious and colorful fried rice.",
    unitPrice: 500,
    quantity: 1,
    image: "/assest/plaintain.png",
    selectedLocation: "agege",
  },
  {
    id: 9,
    name: "Vegetable Soup",
    desc: "Hot, fresh, and extra cheesy.",
    unitPrice: 800,
    quantity: 1,
    image: "/assest/veg.png",
    selectedLocation: "agege",
  },
]);

// DISPLAY-ONLY (no qty/price) but WITH location + order button
const displayFoods = reactive([
 {
  id: 101,
  name: "Eba & Egusi",
  desc: "Hot, smooth eba served with rich, flavourful egusi soup.",
  image: "/assest/ebas.png",
  selectedLocation: "agege",
},
{
  id: 102,
  name: "Efo Riro",
  desc: "Rich, vibrant spinach stew cooked with assorted proteins.",
  image: "/assest/gber.png",
  selectedLocation: "agege",
},
{
  id: 103,
  name: "Fried rice, Jollof, plaintain & Fish",
  desc: "A delicious blend of rice.",
  image: "/assest/frc.png",
  selectedLocation: "agege",
},
{
  id: 104,
  name: "Yam & Egg Sauce",
  desc: "Soft boiled yam paired with tasty, peppered egg sauce.",
  image: "/assest/eggpl.png",
  selectedLocation: "agege",
},
{
  id: 105,
  name: "Plaintain & Egg Sause",
  desc: "Tender yam slices served with spicy, flavourful turkey.",
  image: "/assest/yamegg.png",
  selectedLocation: "agege",
},
{
  id: 106,
  name: "Efo Riro",
  desc: "Rich, vibrant spinach stew cooked with assorted proteins.",
  image: "/assest/soupefo.png",
  selectedLocation: "agege",
},
]);

// Generate WhatsApp link for MAIN CARDS
const generateWhatsAppLink = (food) => {
  const number = locationNumbers[food.selectedLocation];
  if (!number) return "#";
  const text = `I want to order ${food.quantity} portion(s) of ${food.name} for ₦${(
    food.unitPrice * food.quantity
  ).toLocaleString()} from ${food.selectedLocation.toUpperCase()} branch`;
  return `https://wa.me/${number}?text=${encodeURIComponent(text)}`;
};

// Generate WhatsApp link for DISPLAY-ONLY CARDS (no qty/price)
const generateSimpleWhatsAppLink = (item) => {
  const number = locationNumbers[item.selectedLocation];
  if (!number) return "#";
  const text = `Hello, I want to order ${item.name} from ${item.selectedLocation.toUpperCase()} branch.`;
  return `https://wa.me/${number}?text=${encodeURIComponent(text)}`;
};
</script>

<style>
/* Tailwind-only styles */
</style>
