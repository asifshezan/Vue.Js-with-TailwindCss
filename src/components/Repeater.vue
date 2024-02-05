<script setup>

import {ref, reactive} from "vue";

const students = reactive ([
    {name: "Asif Ahamed", gender: "Male"}
]);

const addNewStudents = () => {
    students.push({ name:"", gender:""});
};

</script>

<template>
    <div>
        <p class="p-3">{{ students }}</p>
        <div class="bordered rounded gap-10 p-3">
            <p class="p-3">Students</p>
            <div v-for="(student, index) in students" :key="index">
                <label class="p-3">Name: </label><input type="text" v-model="student.name">

                <label class="p-3"><input type="radio" v-model="student.gender" value="Male"><span class="p-3">Male</span></label>
                <label class="p-3"><input type="radio" v-model="student.gender" value="Female"><span class="p-3">FeMale</span></label>

                <button class="block rounded border m-4 p-4" @click="addNewStudents()">Add New Student</button>
            </div>
        </div>
        
    </div>
</template>

<style scoped></style>
