<script setup>
    import {ref, reactive} from 'vue';

    const choose = ref(0);

    const persons = reactive([
        { name: 'Asif', age:26, city:'USA'},
        { name: 'Arwaa', age: 20, city:'BD'},
        { name: 'Azzan', age: 15, city:'uk'},
    ]);
</script>

<template>
    <div>
        <p class="p-4"> Your Selection Form</p>
        <div class="border rounded p-4 gap-6">
            <p>{{ persons }}</p>
            <p>Choose Person</p>
            <select v-model="choose">
                <option v-for="(person, index) in persons" :key="index" :value="index">{{ person.name }}</option>
            </select>
            <span>Name: </span><input type="text" v-model="persons[choose].name">
            <span>Age: </span><input type="text" v-model="persons[choose].age">
            <span>City: </span><input type="text" v-model="persons[choose].city">
        </div>
    </div>
</template>

<style>

</style>