<template>
  <header id="section">
    <GoToHome />
    <h1>{{ $props.name }}</h1>
  </header>
</template>

<script setup lang="ts">
import GoToHome from './GoToHome.vue';

defineProps<{
  name: string
}>()
</script>

<style scoped>
header {
  position: relative;
}

a {
  position: absolute;
  top: 50%;
  left: 0;
  display: block;
  transform: translateY(-50%);
}
</style>