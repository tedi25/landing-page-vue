<template>
  <header id="navbar-wrapper" class="sticky top-0 left-0 w-full z-10 bg-white shadow-md">
    <nav class="flex items-center py-3 px-10 justify-between md:py-5 md:px-48">
      <!-- Logo -->
      <a href="#">
        <img src="@/assets/logo.png" alt="Logo" class="h-8 md:h-10" />
      </a>

      <!-- Menu -->
      <ul class="hidden md:flex md:flex-row gap-6 text-gray-500">
        <!-- Home -->
        <li class="relative">
          <a href="#">Home</a>
        </li>

        <!-- About -->
        <li class="relative">
          <a href="#">About</a>
        </li>

        <!-- Promotions -->
        <li class="relative">
          <span
            class="absolute -top-4 left-1/2 transform -translate-x-1 bg-red-500 text-white text-xs px-2 py-0.5 rounded-full"
            >HOT</span
          >
          <a href="#">Promotions</a>
        </li>

        <!-- Blogs -->
        <li class="relative">
          <a href="#">Blogs</a>
        </li>

        <!-- Contact Us -->
        <li class="relative">
          <a href="#">Contact Us</a>
        </li>
      </ul>
      <!-- Buttons -->
      <div class="flex items-center space-x-4">
        <button class="hidden md:block cursor-pointer text-gray-800">Masuk</button>
        <ButtonComponent
          outlineColor="hover:outline-1"
          bgColor="bg-primary-green"
          textColor="text-white"
          hoverBg="hover:bg-white"
          hoverOutline="hover:outline-primary-green"
          hoverText="hover:text-primary-green"
          >Daftar Sekarang</ButtonComponent
        >
      </div>

      <!-- Mobile Menu Button -->
      <!-- <button @click="toggleMenu" class="md:hidden text-gray-800">☰</button> -->
    </nav>
  </header>
</template>
<script setup>
import ButtonComponent from './ui/ButtonComponent.vue'
</script>
