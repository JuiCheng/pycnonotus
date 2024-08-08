<template>
  <div
    :class="[
      'h-1/6 w-full  bg-black transition-transform',
      { 'translate-y-[0.625rem] rotate-45 transform': props.isHamburgerOpen }
    ]"
  />
  <div
    :class="['h-1/6 w-2/3  bg-black transition-opacity', { 'opacity-0': props.isHamburgerOpen }]"
  />
  <div
    :class="[
      'h-1/6 w-full  bg-black transition-transform',
      { '-translate-y-[0.625rem] -rotate-45 transform': props.isHamburgerOpen }
    ]"
  />
</template>
<script setup>
const props = defineProps({
  isHamburgerOpen: {
    type: Boolean,
    required: true
  }
})
</script>
