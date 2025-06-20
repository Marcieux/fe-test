<template>
  <section
    class="h-screen relative bg-cover bg-center flex items-center justify-center text-center px-4"
    :style="{ backgroundImage: `url(${banner})` }"
  >
    <div class="text-white flex flex-col items-center">
      <p
        class="text-9xl max-sm:text-7xl max-md:text-7xl max-lg:text-8xl max-xl:text-9xl font-rollie mb-6 drop-shadow-lg leading-tight"
      >
        Passion Craft
      </p>

      <button
        class="cursor-pointer px-8 py-4 bg-white text-black font-semibold rounded-full uppercase font-cromlin text-sm sm:text-base hover:bg-gray-200 transition"
      >
        Order Now
      </button>

      <!-- More Button -->
      <button
        @click="scrollToCategory"
        class="absolute bottom-12 font-cromlin font-bold flex uppercase items-center cursor-pointer gap-2 text-white hover:opacity-80 transition mt-10"
      >
        More
        <svg
          xmlns="http://www.w3.org/2000/svg"
          class="w-4 h-4"
          viewBox="0 0 512 512"
          fill="currentColor"
        >
          <path
            d="M233.4 406.6c12.5 12.5 32.8 12.5 45.3 0l192-192c12.5-12.5 
          12.5-32.8 0-45.3s-32.8-12.5-45.3 0L256 338.7 
          86.6 169.4c-12.5-12.5-32.8-12.5-45.3 0s-12.5 
          32.8 0 45.3l192 192z"
          />
        </svg>
      </button>
    </div>
  </section>
</template>

<script>
import banner from '../assets/banner.jpg';

export default {
  name: "HeroSection",
  data() {
    return {
      banner,
    };
  },
  methods: {
    scrollToCategory() {
      const el = document.getElementById('category-section');
      if (el) {
        el.scrollIntoView({ behavior: 'smooth' });
      }
    },
  },
};
</script>
