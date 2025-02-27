<template>
  <div class="flex flex-col gap-10">
    <div id="text-content" class="flex flex-col gap-2">
      <h1 class="text-2xl md:text-4xl font-medium text-primary-green">Browse Our Trending</h1>
      <h1 class="text-2xl md:text-4xl font-medium">Receipt</h1>
    </div>
    <div
      id="trending-menu"
      class="grid grid-cols-1 md:grid-cols-4 justify-items-stretch gap-6 rounded-2xl"
    >
      <div
        v-for="(item, index) in trending"
        :key="index"
        :class="[item.bgColor]"
        id="card-menu"
        class="h-[390px] px-6 rounded-2xl w-full bg-none shadow-2xl md:px-8 flex flex-col gap-4 justify-center hover:bg-[url(../assets/bg-main.png)] hover:bg-cover hover:bg-blend-soft-light"
      >
        <img :src="item.imgSrc" alt="" class="object-cover bg-cover w-36 h-auto" />
        <h1 class="text-3xl text-black">{{ item.name }}</h1>
        <h2 class="text-xl text-gray-400">{{ item.type }}</h2>
        <img :src="item.stars" alt="" class="object-cover w-20" />
      </div>
    </div>
    <div id="button" class="self-center">
      <ButtonComponent
        outlineColor="hover:outline-1"
        bgColor="bg-primary-green"
        textColor="text-white"
        hoverBg="hover:bg-white"
        hoverOutline="hover:outline-primary-green"
        hoverText="hover:text-primary-green"
        >ALL Receipt</ButtonComponent
      >
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'
import ButtonComponent from '@/components/ui/ButtonComponent.vue'
import Four from '@/assets/icons/four-stars.png'
import Three from '@/assets/icons/three-stars.png'
import Five from '@/assets/icons/five-stars.png'
import CupcakeChoco from '@/assets/images/cupcake-choco.png'
import DonerKebab from '@/assets/images/doner-kebab.png'
import DoughnutMilk from '@/assets/images/doughnut-milk.png'
import DoughnutUnicorn from '@/assets/images/dougnut-unicorn.png'
import KathiKebab from '@/assets/images/kathi-kebab.png'
import SalmonRoll from '@/assets/images/salmon-roll.png'
import PizzaMeat from '@/assets/images/pizzameat.png'
import PizzaPaperoni from '@/assets/images/pizzapaperoni.png'

const trending = ref([
  {
    name: 'Pizza Paperoni',
    type: 'Pizza',
    bgColor: 'bg-soft-primary-teal',
    imgSrc: PizzaPaperoni,
    stars: Four,
  },
  {
    name: 'Pizza Meat',
    type: 'Pizza',
    bgColor: 'bg-soft-primary-teal',
    imgSrc: PizzaMeat,
    stars: Three,
  },
  {
    name: 'Doner Kebab',
    type: 'Kebab',
    bgColor: 'bg-soft-primary-blue',
    imgSrc: DonerKebab,
    stars: Five,
  },
  {
    name: 'Salmon Roll',
    type: 'Salmon',
    bgColor: 'bg-soft-primary-magenta',
    imgSrc: SalmonRoll,
    stars: Four,
  },
  {
    name: 'Cupcake Choco',
    type: 'Cupcake',
    bgColor: 'bg-soft-primary-green',
    imgSrc: CupcakeChoco,
    stars: Four,
  },
  {
    name: 'Doughnut Milk',
    type: 'Doughnut',
    bgColor: 'bg-soft-primary-lightgreen',
    imgSrc: DoughnutMilk,
    stars: Five,
  },
  {
    name: 'Doughnut Unicorn',
    type: 'Doughnut',
    bgColor: 'bg-soft-primary-lightgreen',
    imgSrc: DoughnutUnicorn,
    stars: Four,
  },
  {
    name: 'Kathi Kebab',
    type: 'Kebab',
    bgColor: 'bg-soft-primary-blue',
    imgSrc: KathiKebab,
    stars: Four,
  },
])
</script>
