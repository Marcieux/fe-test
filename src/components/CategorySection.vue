<template>
  <section
    id="category-section"
    class="min-h-screen flex justify-center items-center text-center px-4 py-16"
  >
    <div
      class="w-full grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-6 font-rollie text-white max-sm:py-24 max-md:py-24 max-lg:py-24 max-xl:py-24"
    >
      <!-- Birthday Cake -->
      <div
        class="relative w-full max-w-sm mx-auto bg-cover bg-center bg-gray-100 h-120 rounded-xl shadow-md hover:shadow-xl transition"
        :style="{ backgroundImage: `url(${birthdayCake})` }"
      >
        <span
          class="absolute w-full bottom-6 left-1/2 transform -translate-x-1/2 text-4xl max-sm:text-3xl drop-shadow"
        >
          Birthday Cakes
        </span>
      </div>

      <!-- Wedding Cake -->
      <div
        class="relative w-full max-w-sm mx-auto bg-cover bg-center bg-gray-100 h-120 rounded-xl shadow-md hover:shadow-xl transition"
        :style="{ backgroundImage: `url(${weddingCake})` }"
      >
        <span
          class="absolute w-full bottom-6 left-1/2 transform -translate-x-1/2 text-4xl max-sm:text-3xl drop-shadow"
        >
          Wedding Cakes
        </span>
      </div>

      <!-- Christmas Cake -->
      <div
        class="relative w-full max-w-sm mx-auto bg-cover bg-center bg-gray-100 h-120 rounded-xl shadow-md hover:shadow-xl transition"
        :style="{ backgroundImage: `url(${christmasCake})` }"
      >
        <span
          class="absolute w-full bottom-6 left-1/2 transform -translate-x-1/2 text-4xl max-sm:text-3xl drop-shadow"
        >
          Christmas Cakes
        </span>
      </div>
    </div>
  </section>
</template>

<script>
import birthdayCake from "../assets/birthdaycake.jpg";
import weddingCake from "../assets/weddingcake.jpg";
import christmasCake from "../assets/christmascake.jpg";

export default {
  name: "CategorySection",
  data() {
    return {
      birthdayCake,
      weddingCake,
      christmasCake,
    };
  },
};
</script>
