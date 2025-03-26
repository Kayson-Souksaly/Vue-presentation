<template>
  <div class="mb">
    <img src="../assets/codeImage/refCode1.png" alt="Ref() Code Block" class="mb-5" />
    <img src="../assets/codeImage/refCode2.png" alt="Ref() Code Block" class="mb-5" />

    <h1 class="text-danger">Code Example</h1>
    <!-- Display a reactive message -->
    <h2>{{ message }}</h2>

    <!-- Button updates the message using the greeting value -->
    <button @click="message = greeting" class="btn btn-success">Click Me!</button>
  </div>
</template>

<script setup>
// Import ref to create a reactive primitive
import { ref } from 'vue'

// Create a reactive variable using ref()
// The default value is shown on the screen
const message = ref('Hello User!')

// Non-reactive string value to replace the message when the button is clicked
const greeting = 'How was your day?'
</script>

<style scoped>
div {
  text-align: center;
}
</style>
