<template>
  <RouterLink :to="props.path">{{ props.name }}</RouterLink>
</template>

<script setup lang="ts">
import { RouterLink } from 'vue-router';

const props = defineProps<{
  path: string,
  enabled: boolean,
  name: string
}>()
</script>

<style scoped>

</style>