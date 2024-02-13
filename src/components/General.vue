<script setup>

import { ref, reactive } from 'vue';

const inputt = ref('test');

const inputt2 = ref('test2');

const inputt3 = ref('test3');

const check = ref([])

const radio = ref('')

const select = ref('')

</script>

<template>

<div>
    <p class="p-4">Output: {{ inputt }}</p>
    <span class="p-4">Input: </span><input type="text" v-model="inputt">

    <p class="p-4">Output: {{ check }}</p>
    <span class="p-4">Input: </span>
    <label><input type="checkbox" v-model="check" value="class">Class</label>
    <label for=""><input type="checkbox" v-model="check" value="record">Record</label>

    <p class="p-4">Output: {{ radio }}</p>
    <span class="p-4">Class </span><input type="radio" v-model="radio" value="class">
    <span class="p-4">Record </span><input type="radio" v-model="radio" value="record">

    <p class="p-4">Select: {{ select }}</p>
    <select name="" id="" v-model="select">
        <option value="1">1</option>
        <option value="2">2</option>
        <option value="3">3</option>
        <option value="4">4</option>
    </select>


    <p class="p-4">Output: {{ inputt2 }}</p>
    <span class="p-4">Input: </span><input type="text" v-model.trim="inputt2">

    <p class="p-4">Output: {{ inputt3 }}</p>
    <span class="p-4">Input: </span><input type="text" v-model.number="inputt3">
</div>

</template>

<style scoped>

</style>