<script setup>
import HelloWorld from './components/HelloWorld.vue'
import General from './components/General.vue'
import Select from './components/Select.vue'
import Quiz from './components/Quiz.vue'
import Repeater from './components/Repeater.vue'

</script>

<template>
  <div class="container">
  <div class="flex">
    <a href="https://vitejs.dev" target="_blank">
      <img src="/vite.svg" class="logo" alt="Vite logo" />
    </a>
    <a href="https://vuejs.org/" target="_blank">
      <img src="./assets/vue.svg" class="logo vue" alt="Vue logo" />
    </a>
  </div>
</div>
  <HelloWorld msg="Vite + Vue" />
  <General />
  <Select />
  <Quiz />
  <Repeater />

</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
