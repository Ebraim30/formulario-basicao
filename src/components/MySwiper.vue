<script setup>
// import Swiper core and required modules
import { Pagination } from 'swiper';

// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from 'swiper/vue';

// Import Swiper styles
import 'swiper/css';
import 'swiper/css/pagination';

const modules = [Pagination]



</script>

<template>
  <swiper :modules="modules" :slides-per-view="1" :pagination="{ clickable: true }" class="pb-10">
    <swiper-slide class="grid place-items-center">
      <img src="../assets/maenatureza/KIDS.jpeg" class="w-22 h-30% lg:w-[90%] mt-20 rounded-full" />
    </swiper-slide>
    <swiper-slide class="grid place-items-center">
      <img src="../assets/maenatureza/LAB.jpeg" class="w-22 h-30% lg:w-[90%] mt-20 rounded-full" />
    </swiper-slide>
    <swiper-slide class="grid place-items-center">
      <img src="../assets/maenatureza/MEDIO.jpeg" class="w-22 h-30% lg:w-[90%] mt-20 rounded-full" />
    </swiper-slide>
  </swiper>
</template>

<style>
.swiper-pagination-bullet {
  @apply w-3 h-3 bg-white opacity-100
}

.swiper-pagination-bullet.swiper-pagination-bullet-active {
  @apply rounded-xl w-6 bg-secondary
}
</style>