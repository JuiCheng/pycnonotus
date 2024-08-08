<template>
  <div
    class="relative flex h-[311px] w-full flex-col items-center justify-end bg-[url(/background.png)] bg-cover bg-no-repeat 2xl:h-2/3 2xl:items-end 2xl:pb-5 2xl:pr-20"
  >
    <!--Banner Rectangle 3 -->
    <div class="absolute inset-0 bg-[rgba(0,0,0,0.1)]"></div>
    <div class="w-[87%] 2xl:flex 2xl:justify-end 2xl:gap-2">
      <!-- Title -->
      <h3 class="text-right text-5xl font-bold text-white 2xl:text-6xl">
        {{ props.titleInfo.ChineseName }} {{ props.titleInfo.EnglishName }}
      </h3>
    </div>

    <p class="my-3 w-[87%] text-right text-lg text-white 2xl:text-xl">
      {{ props.titleInfo.Caption }}
    </p>
  </div>
</template>

<script setup>
const props = defineProps({
  titleInfo: {
    type: Object,
    required: true
  }
})
</script>
