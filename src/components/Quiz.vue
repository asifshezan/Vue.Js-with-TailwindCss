<script setup>

import {ref, reactive} from "vue";

const score = ref(0);

const questions = reactive ([
    { desc: "Is the 1st answer is true?", answer: "yes"},
    { desc: "Is the 2nd answer is true?", answer: "no"},
    { desc: "Is the 3rd answer is true?", answer: "yes"},
    { desc: "Is the 4th answer is true?", answer: "no"},
    { desc: "Is the 5th answer is true?", answer: "yes"},
]);

const calculatedValue = () => {
    score.value = 0;

    questions.forEach(question => {
        if(question.answer == question.input){
           score.value = score.value + 1;
        }
    });
}

</script>

<template>
    <div>
        <p class="p-4"> Your Score: {{ score }}</p>
        
        <div v-for="(question,index) in questions" :key="index" class="border rounded p-4 gap-10">
            <p class="p-3">{{ question.desc }}</p>

            <label class="p-3">
                <input type="radio" class="pr-3" value="yes" @change="calculatedValue()" v-model="question.input"><span class="pl-2">Yes</span>
            </label>
            <label class="p-3">
                <input type="radio" class="pr-3" value="no" @change="calculatedValue()" v-model="question.input"><span class="pl-2">No</span>
            </label>
        </div>
    </div>
</template>

<style scoped>

</style>