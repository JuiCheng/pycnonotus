<script setup>
import { RouterView } from 'vue-router'
import NavbarComponent from './components/NavbarComponent.vue'
</script>

<template>
  <div class="flex min-h-screen flex-col xl:flex-row">
    <NavbarComponent></NavbarComponent>
    <RouterView />
  </div>
</template>
