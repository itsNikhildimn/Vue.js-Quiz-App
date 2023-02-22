<script setup>
import { defineProps } from 'vue';
import { useRouter } from 'vue-router';

const router = useRouter()
const {quiz} = defineProps(['quiz'])

const navigateToQuiz = () => {
  router.push(`/quiz/${quiz.id}`)
}
</script>

<template>
    <div class="card" @click="navigateToQuiz">
        <img :src= "quiz.img" alt="">
      <div class="card-text">
        <h2>{{ quiz.name }}</h2>
        <p>{{ quiz.questions.lenght }}-questions</p>
      </div>
    </div>
</template>

<style scoped>
.card {
  width: 200px;
  height:250px;
  overflow: hidden;
  border-radius: 2%;
  box-shadow: 1px 1px 10px black;
  margin-bottom: 35px;
  margin-right: 20px;
  cursor: pointer;
}
img{
  width: 100%;
  height: 180px;
}
.card-text{
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding:0 0.5rem;
}
</style>