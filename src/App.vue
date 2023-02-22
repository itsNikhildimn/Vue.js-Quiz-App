<script setup>
import { RouterView } from 'vue-router';
import QuizesView from "./views/QuizesView.vue"
</script>

<template>
  <div class="conatiner">
    <RouterView/>
<!-- <QuizesView/>/ -->
  </div>
</template>

<style scoped>
.container {
  max-width: 1000px;
margin: auto;
}
</style>