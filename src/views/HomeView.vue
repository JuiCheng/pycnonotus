<template>
  <main class="flex flex-col xl:min-h-screen xl:w-3/4">
    <Banner :titleInfo="titleInfo"> </Banner>
    <div
      class="flex min-h-fit w-full flex-col items-center gap-[50px] bg-[#dcccbc] py-[50px] xl:h-1/3 xl:min-h-0 xl:flex-row xl:items-start xl:justify-around xl:py-[60px]"
    >
      <Intro
        v-for="(intro, index) in introList"
        :key="index"
        :title="intro.title"
        :description="intro.description"
      />
    </div>
  </main>
</template>

<script setup>
import Banner from '../components/BannerComponent.vue'
import Intro from '../components/IntroComponent.vue'

const titleInfo = {
  ChineseName: '白頭翁',
  EnglishName: '(Chinese bulbul)',
  Caption: '又名白頭鵯。以果實、昆蟲為主食，無法消化小米、穀類。平均壽命約 8~10 年。',
  BannerImage: '/background.png'
}

const introList = [
  {
    title: '外觀',
    description:
      '白頭鵯體長約17到22公分，額至頭頂純黑色而富有光澤，兩眼上方至後枕白色，形成一白色枕環。耳羽後部有一白斑，此白環與白斑在黑色的頭部均極為醒目，老鳥的枕羽(後頭部)更潔白，所以又叫「白頭翁」。'
  },
  {
    title: '棲地',
    description:
      '白頭翁和麻雀、綠繡眼合稱「城市三寶」，常成群出現在平原區灌木叢、丘陵樹林地帶，以及校園、公園、庭院、行道中的各種高高的電線與樹上。'
  },
  {
    title: '食性',
    description:
      '以果樹的漿果和種子為主食，並時常飛入果園偷吃果實，還會吃嫩葉嫩芽，尤其是胡蝶蘭的嫩葉嫩芽葉，偶爾啄食昆蟲。'
  }
]
</script>
