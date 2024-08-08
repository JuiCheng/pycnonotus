<template>
  <main class="flex flex-col xl:min-h-screen xl:w-3/4">
    <Banner :titleInfo="titleInfo"> </Banner>
  </main>
</template>

<script setup>
import Banner from '../components/BannerComponent.vue'

const titleInfo = {
  ChineseName: '白頭翁',
  EnglishName: '(Chinese bulbul)',
  Caption: '又名白頭鵯。以果實、昆蟲為主食，無法消化小米、穀類。平均壽命約 8~10 年。',
  BannerImage: '/background.png'
}
</script>
