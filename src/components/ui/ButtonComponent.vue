<template>
  <button
    class="px-4 py-2 md:px-5 md:py-3 rounded-full cursor-pointer transition-all"
    :class="[bgColor, textColor, hoverBg, hoverText, hoverOutline, outlineColor]"
  >
    <slot></slot>
  </button>
</template>

<script setup>
defineProps({
  bgColor: String,
  textColor: String,
  hoverBg: String,
  hoverText: String,
  hoverOutline: String,
  outlineColor: String,
})
</script>
