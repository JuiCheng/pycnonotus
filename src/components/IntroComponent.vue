<template>
  <div
    class="mx-9 flex w-full items-start justify-between px-7 md:px-24 lg:px-60 xl:mx-0 xl:w-fit xl:justify-center xl:gap-10 xl:px-0"
  >
    <div class="relative">
      <p class="text-4xl font-bold [writing-mode:vertical-lr]">{{ props.title }}</p>
      <!-- circle decoration -->
      <div
        class="absolute bottom-[-0.75rem] left-[25px] h-6 w-6 rounded-full border-8 border-opacity-orange bg-transparent"
      ></div>
    </div>

    <div class="w-[75%] font-normal xl:w-[200px]">
      <p>{{ props.description }}</p>
    </div>
  </div>
</template>

<script setup>
const props = defineProps({
  title: {
    type: String,
    required: true
  },
  description: {
    type: String,
    required: true
  }
})
</script>
