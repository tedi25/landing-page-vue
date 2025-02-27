<template>
  <div
    id="wrapper-hero-section"
    class="relative grid px-10 py-10 grid-cols-1 gap-5 md:grid-cols-[1fr_2fr] md:px-48 md:gap-10"
  >
    <div id="hero-title" class="flex text-primary-green self-end md:order-1">
      <h1 class="text-5xl md:text-7xl font-medium">Good Food Us <br />Good Mood</h1>
    </div>
    <div id="hero-image " class="row-span-2 md:justify-self-end md:order-2">
      <img src="@/assets/green-salat-fix.png" class="h-full bg-cover w-70 md:w-2xl" alt="" />
      <div id="mini-card" class="absolute bottom-1/3 right-10 md:bottom-28 md:left-1/2">
        <MiniCardComponent />
      </div>
    </div>
    <div id="hero-sub-title" class="flex flex-col gap-6 md:gap-10 order-3 md:order-3">
      <h2 class="text-lg font-light text-gray-500">
        I would think that conserving our natural resources should be a conservative position: Not
        to waste food, and not to throw away a lot of the food that we buy
      </h2>
      <div id="button-group" class="group flex gap-4">
        <ButtonComponent
          outlineColor="hover:outline-1"
          bgColor="bg-primary-green"
          textColor="text-white"
          hoverBg="hover:bg-white"
          hoverOutline="hover:outline-primary-green"
          hoverText="hover:text-primary-green"
          >Daftar Sekarang</ButtonComponent
        >
        <ButtonComponent
          outlineColor="hover:outline-1"
          bgColor="bg-gray-200"
          textColor="text-black"
          hoverBg="hover:bg-black"
          hoverOutline="hover:outline-black"
          hoverText="hover:text-gray-200"
          >About Us</ButtonComponent
        >
      </div>
    </div>
  </div>
</template>

<script setup>
import MiniCardComponent from './MiniCardComponent.vue'
import ButtonComponent from './ui/ButtonComponent.vue'
</script>
