<template>
  <div class="app">
    <Sidebar />

    <router-view />
  </div>
</template>

<script setup>
import Sidebar from './components/Sidebar.vue'
import Tabla from './components/Tabla.vue';
import Opciones from './components/Opciones.vue';
</script>

<style lang="scss">
:root {
  --primary: #4ade80;
  --primary-alt: #22c55e;
  --grey: #64748b;
  --dark: #2b323a;
  --dark-alt: #334155;
  --light: #ffffff;
  --sidebar-width: 300px;
  --button: #f46516;
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Fira sans', sans-serif;
}

body {
  background: var(--light);
}

button {
  cursor: pointer;
  appearance: none;
  border: none;
  outline: none;
  background: none;
}

.app {
  display: flex;

  main {
    flex: 1 1 0;
    padding: 2rem;

    @media (max-width: 1024px) {
      padding-left: 6rem;
    }
  }
}
</style>