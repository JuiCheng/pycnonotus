<template>
  <div
    :style="{ backgroundImage: `url('${props.titleInfo.BannerImage}')` }"
    class="relative flex h-[311px] w-full flex-col items-center justify-end bg-cover bg-no-repeat xl:h-2/3 xl:items-end xl:pb-5 xl:pr-20"
  >
    <!--Banner Rectangle 3 -->
    <div class="absolute inset-0 bg-[rgba(0,0,0,0.1)]"></div>
    <div class="w-[87%] xl:flex xl:justify-end xl:gap-2">
      <!-- Title -->
      <h3 class="text-right text-5xl font-bold text-white xl:text-6xl">
        {{ props.titleInfo.ChineseName }} {{ props.titleInfo.EnglishName }}
      </h3>
    </div>

    <p class="my-3 w-[87%] text-right text-lg text-white xl:text-xl">
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
