<template>
  <header>
    <nav>
      <RouterLink v-for="(route, index) in routes" :to="route.path" :key="index" active-class="active"
        :class="{ disabled: index % 2 === 0 }">{{ route.name }}</RouterLink>
    </nav>
  </header>
</template>

<script setup lang="ts">
import { RouterLink } from 'vue-router';

const routes = [
  { path: '/', name: 'Inicio' },
  { path: '/about', name: 'Nosotros' },
  { path: '/gallery', name: 'Galería' },
  { path: '/services', name: 'Servicios' },
  { path: '/testimonials', name: 'Testimonios' },
  { path: '/clients', name: 'Clientes' }
];
</script>

<style scoped>
a:hover {
  color: #525252;
}

a {
  border-radius: 24px;
  padding: 4px 12px;
}

header {
  width: 100%;
  display: flex;
  justify-content: center;
}

nav {
  display: flex;
  gap: 12px;
}

.disabled {
  background-color: transparent;
  pointer-events: none;
  color: #737373;
}

.active {
  background-color: #0a0a0a;
  color: white;
}

.active:hover {
  background-color: #0a0a0a;
  color: white;
}
</style>