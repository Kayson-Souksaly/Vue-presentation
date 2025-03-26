<template>
  <div class="mb">
    <h2>{{ message }}</h2>

    <button @click="message = greeting" class="btn btn-success">Click Me!</button>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const message = ref('Hello User!')

const greeting = 'How was your day?'
</script>

<style scoped>
div {
  text-align: center;
}
button {
  font-size: 1.5em;
}
</style>
