<template>
  <header>
    <a href="https://vuejs.org/" target="_blank">
      <img src="./assets/vue.svg" class="logo vue" alt="Vue logo" />
    </a>
    <h1>Vue</h1>
  </header>
  <main>
    <Parent />
  </main>
</template>

<script setup>
import Parent from "./components/Parent.vue"
</script>

<style scoped>
.logo {
  height: 5em;
  padding: 1em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.react:hover {
  filter: drop-shadow(0 0 2em #61dafbaa);
}
</style>