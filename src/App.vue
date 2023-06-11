<script setup>
import { ref, computed } from 'vue'

const questions = ref([
    {
      question: 'who won in the MR headset',
      answer: 0,
      options: [
       'Meta',
       'Apple',
       'Twitter'
      ],
      selected: null 
    },
    {
      question: 'who raps in Nigeria',
      answer: 0,
      options: [
       'Blaqbonez',
       'Falz',
       'Rema'
      ],
      selected: null 
    },
    {
      question: 'Which state is big in nigeria?',
      answer: 1,
      options: [
       'Lagos',
       'Kano',
       'Abuja'
      ],
      selected: null 
    },
    {
      question: 'will self driving car win?',
      answer: 0,
      options: [
       'Yes',
       'No',
       'Maybe'
      ],
      selected: null 
    },



])

const quizCompleted = ref(false)
const currentQuestion = ref(0)
const score = computed(() => {
  let value = 0
  question.value.map(q => {
    if (q.selected == q.answer){
      value++
    }
  })
  return value 
})


const getCurrentQuestion = computed(() => {
  let question = questions.value(currentQuestion.value)
  question.index = currentQuestion.value
  return question 
})


</script>

<template>
  
</template>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Montserrat', sans-serif;
}

body {
  background-color: #271c36;
  color:#FFF;
}
</style>
