<template>
  <div
    class="relative z-10 min-h-[87px] w-screen bg-white shadow-[0_5px_5px_0px_rgba(0,0,0,0.25)] xl:h-screen xl:w-1/4"
  >
    <div class="flex items-center justify-around py-5">
      <div
        class="hamburger flex h-[1.5rem] w-[1.5rem] cursor-pointer flex-col justify-between xl:hidden"
        @click="toggleHamburger"
      >
        <HamburgerIcon :isHamburgerOpen="isHamburgerOpen"></HamburgerIcon>
      </div>
      <h3 class="text-xl font-bold xl:mt-[4rem] xl:text-3xl">白頭翁不吃小米</h3>
      <Logo />
    </div>
    <ul
      :class="[
        'flex w-full flex-col items-center gap-3 bg-white transition-all duration-300 xl:mt-20 xl:max-h-fit xl:opacity-100',
        {
          'max-h-0 opacity-0': !isHamburgerOpen,
          'max-h-[200px] pb-[50px] opacity-100': isHamburgerOpen
        }
      ]"
    >
      <li
        v-for="link in linkList"
        :key="link.name"
        :class="[
          'text-lg font-bold hover:text-orange-400',
          { 'text-[#AA6666] underline': pathname === link.href }
        ]"
      >
        <a :href="link.href">{{ link.name }}</a>
      </li>
    </ul>
  </div>
</template>

<script setup>
import { ref, computed } from 'vue'
import { useRoute } from 'vue-router'
import Logo from './icons/LogoIconComponent.vue'
import HamburgerIcon from './icons/HamburgerIconComponent.vue'

const isHamburgerOpen = ref(false)
const route = useRoute()
const pathname = computed(() => route.path)

const toggleHamburger = () => {
  isHamburgerOpen.value = !isHamburgerOpen.value
}

const linkList = ref([
  { name: '白頭翁的特性', href: '/' },
  { name: '白頭翁的生態', href: '/ecology' },
  { name: '白頭翁的美照', href: '/gallery' },
  { name: '白頭翁的危機', href: '/crisis' }
])
</script>
