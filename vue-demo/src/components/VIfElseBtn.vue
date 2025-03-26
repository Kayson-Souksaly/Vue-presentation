<template>
  <div>
    <img src="../assets/codeImage/v-ifCode.png" alt="v-if Code Block" class="mb-5" />
    <img src="../assets/codeImage/v-ifCode2.png" alt="v-if Code Block" class="mb-5" />

    <h1 class="text-danger">Code Example</h1>
    <!-- Conditional rendering of animal image based on selection -->
    <div class="image-container">
      <!-- Show bird image if 'bird' is selected -->
      <img src="../assets/bird.jpg" alt="bird" v-if="animal === 'bird'" />

      <!-- Show dog image if 'dog' is selected -->
      <img src="../assets/dog.jpg" alt="dog" v-else-if="animal === 'dog'" />

      <!-- Show cat image if 'cat' is selected -->
      <img src="../assets/cat.jpg" alt="cat" v-else-if="animal === 'cat'" />

      <!-- Show prompt if no animal is selected -->
      <p v-else>Choose an Animal...</p>
    </div>

    <p>Do You Like...</p>

    <!-- Buttons to change the reactive variable 'animal' -->
    <div class="btn-container">
      <button @click="animal = 'bird'" class="btn btn-success me-2">Birds</button>
      <button @click="animal = 'dog'" class="btn btn-success me-2">Dogs</button>
      <button @click="animal = 'cat'" class="btn btn-success">Cats</button>
    </div>
  </div>
</template>

<script setup>
// Import ref to make it reactive
import { ref } from 'vue'

// Reactive variable that stores the selected animal type
const animal = ref('')
</script>

<style>
.image-container {
  width: 100%;
  height: 40vh;
}

img {
  height: 100%;
  width: auto;
}
</style>
