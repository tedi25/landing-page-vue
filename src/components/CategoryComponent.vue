<template>
  <div class="flex flex-col gap-10">
    <div id="text-content" class="flex flex-col gap-2">
      <h1 class="text-2xl md:text-4xl font-medium text-primary-green">Browse Our Category</h1>
      <h1 class="text-2xl md:text-4xl font-medium">Receipt</h1>
    </div>
    <div class="relatives">
      <!-- Carousel Wrapper -->
      <div
        ref="carousel"
        class="relative flex overflow-x-auto snap-x snap-mandatory scroll-smooth space-x-4 w-screen scrollbar-hide"
      >
        <div
          v-for="(item, index) in categories"
          :key="index"
          :class="[item.bgColor]"
          class="w-[230px] h-[175px] flex-none snap-start bg-none rounded-lg flex flex-col py-auto justify-center items-center hover:min-h-[190px] hover:bg-[url(../assets/bg-main.png)] hover:bg-cover hover:bg-blend-soft-light"
        >
          <img :src="item.imgSrc" alt="Category" class="w-[47px] h-[52px] mb-2" />
          <p class="font-medium">{{ item.name }}</p>
          <p class="text-sm text-gray-500">{{ item.items }} Items</p>
        </div>
      </div>
    </div>
    <div id="nav-button" class="hidden md:flex md:gap-2 md:self-end">
      <button
        @click="prevSlide()"
        class="flex cursor-pointer flex-row items-center gap-2 rounded-full bg-primary-green px-4 py-2"
      >
        <img src="../assets/icons/left-arrow.png" class="h-[33px] w-[33px] object-cover" alt="" />
        <span class="text-white">PREV</span>
      </button>
      <button
        @click="nextSlide()"
        class="flex cursor-pointer flex-row items-center gap-2 rounded-full bg-primary-green px-4 py-2"
      >
        <span class="text-white">NEXT</span>
        <img src="../assets/icons/right-arrow.png" class="h-[34px] w-[34px] object-cover" alt="" />
      </button>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'
import Cookie from '@/assets/icons/cookie.png'
import Pizza from '@/assets/icons/pizza.png'
import Kebab from '@/assets/icons/kebab.png'
import Salmon from '@/assets/icons/salmon.png'
import Doughnut from '@/assets/icons/doughnut.png'

const carousel = ref(null)

const categories = ref([
  {
    name: 'Cupcake',
    items: 25,
    bgColor: 'bg-soft-primary-green',
    imgSrc: Cookie,
  },
  {
    name: 'Pizza',
    items: 23,
    bgColor: 'bg-soft-primary-teal',
    imgSrc: Pizza,
  },
  {
    name: 'Kebab',
    items: 12,
    bgColor: 'bg-soft-primary-blue',
    imgSrc: Kebab,
  },
  {
    name: 'Salmon',
    items: 22,
    bgColor: 'bg-soft-primary-magenta',
    imgSrc: Salmon,
  },
  {
    name: 'Doughnut',
    items: 15,
    bgColor: 'bg-soft-primary-lightgreen',
    imgSrc: Doughnut,
  },
  {
    name: 'Cupcake',
    items: 25,
    bgColor: 'bg-soft-primary-green',
    imgSrc: Cookie,
  },
  {
    name: 'Pizza',
    items: 23,
    bgColor: 'bg-soft-primary-teal',
    imgSrc: Pizza,
  },
  {
    name: 'Kebab',
    items: 12,
    bgColor: 'bg-soft-primary-blue',
    imgSrc: Kebab,
  },
  {
    name: 'Salmon',
    items: 22,
    bgColor: 'bg-soft-primary-magenta',
    imgSrc: Salmon,
  },
  {
    name: 'Doughnut',
    items: 15,
    bgColor: 'bg-soft-primary-lightgreen',
    imgSrc: Doughnut,
  },
])

const nextSlide = () => {
  if (carousel.value) {
    carousel.value.scrollLeft += 246 // Moves one item forward
  }
}

const prevSlide = () => {
  if (carousel.value) {
    carousel.value.scrollLeft -= 246 // Moves one item backward
  }
}
</script>

<style>
/* Hilangkan scrollbar */
.scrollbar-hide::-webkit-scrollbar {
  display: none;
}
</style>
