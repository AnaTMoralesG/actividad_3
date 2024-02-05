<script setup lang="ts">
import TitleHeader from '@/components/TitleHeader.vue';
import { ref } from 'vue';

const showImage = ref(false)

const handleShowImage = () => {
  showImage.value = !showImage.value
}
</script>

<template>
  <TitleHeader name="Inicio" />
  <section>
    <button @click="handleShowImage">
      {{ showImage ? 'Ocultalo ＞︿＜' : 'Haz click aquí ( •̀ ω •́ )✧' }}
    </button>

    <img v-if="showImage" src="https://i.makeagif.com/media/12-22-2023/NNjPc5.gif" alt="gif">
  </section>
</template>

<style scoped>

section {
  display: flex;
  flex-direction: column;
  place-items: center;
}

button {
  background-color: #0a0a0a;
  padding: 8px 12px;
  color: white;
  border-radius: 4px;
  cursor: pointer;
  margin: 8px 0;
  border: none;
}

img {
  margin: 12px 0;
}
</style>
