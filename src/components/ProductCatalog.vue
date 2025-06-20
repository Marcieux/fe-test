<template>
  <section
    id="product-catalog"
    class="bg-white w-full flex justify-center items-center"
  >
    <div class="w-full">
      <div class="grid grid-cols-2 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4 gap-2">
        <div
          v-for="(cake, index) in cakes"
          :key="index"
          class="relative bg-cover bg-center h-90 shadow-md hover:shadow-xl transition"
          :style="{ backgroundImage: `url(${cake})` }"
        ></div>
      </div>
    </div>
  </section>
</template>

<script>
import cakeOne from "../assets/cake1.jpg";
import cakeTwo from "../assets/cake2.jpg";
import cakeThree from "../assets/cake3.jpg";
import cakeFour from "../assets/cake4.jpg";
import cakeFive from "../assets/cake5.jpg";
import cakeSix from "../assets/cake6.jpg";
import cakeSeven from "../assets/cake7.jpg";
import cakeEight from "../assets/cake8.jpg";

export default {
  name: "ProductCatalog",
  data() {
    return {
      cakes: [
        cakeOne,
        cakeTwo,
        cakeThree,
        cakeFour,
        cakeFive,
        cakeSix,
        cakeSeven,
        cakeEight,
      ],
    };
  },
};
</script>

<style scoped></style>
