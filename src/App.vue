<script setup lang="ts">
import { RouterView } from 'vue-router'
import HeaderMain from './components/HeaderMain.vue';
</script>

<template>
  <HeaderMain />

  <main>
    <RouterView />
  </main>
</template>

<style scoped>
main {
  padding-top: 12px;
  flex-grow: 1;
}
</style>
