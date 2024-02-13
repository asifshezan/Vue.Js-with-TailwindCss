<script setup>
import {ref} from 'vue'
export const name = ref('Vue 3')
// function updateValue(event){
// name.value = event.target.value
// }

export const color = ref('Black')

export function alertTest(){
  alert("Searching "+ name.value)
}
</script>

<template>
<!-- <h1>Two Way Data Binding</h1> -->
<h2>{{ name }}</h2>
<!-- <input type="text" value="name" @input="updateValue($event)"> -->
<input type="text" v-model="name">

<input type="text" v-model="name">

<input type="text" v-model="name">
<button class="bg-blue-500" @click ="alertTest()"> Button </button>


<p>What is your favourite color?</p>
<h3>{{ color }}</h3>
<p>
    <input type="checkbox" v-model="color" true-value="Black">
</p>
</template>
<style scoped>
</style>