<template>
  <NavbarComponent />
  <section
    id="header"
    class="relative bg-[url(../assets/bg-main.png)] md:object-cover md:bg-cover md:bg-no-repeat"
  >
    <div class="absolute inset-0 bg-white/98"></div>
    <HeroComponent />
  </section>
  <section id="category" class="px-10 py-10 md:px-48 md:py-20">
    <CategoryComponent />
  </section>
  <section id="trending" class="px-10 py-10 md:px-48 md:py-20">
    <TrendingComponent />
  </section>
  <section id="footer" class="px-10 py-10 md:px-48 md:py-10">
    <FooterComponent />
  </section>
  <p class="text-center text-gray-400 text-sm">&copy; ELEMES ID. ALL RIGHTS RESERVED</p>
  <FooterNavbarComponent />
</template>

<script setup>
import NavbarComponent from '@/components/NavbarComponent.vue'
import HeroComponent from '@/components/HeroComponent.vue'
import FooterNavbarComponent from '@/components/FooterNavbarComponent.vue'
import CategoryComponent from '@/components/CategoryComponent.vue'
import TrendingComponent from '@/components/TrendingComponent.vue'
import FooterComponent from '@/components/FooterComponent.vue'
</script>
