<template>
  <div>
    <div class="image-container">
      <img src="../assets/bird.jpg" alt="bird" v-if="animal === 'bird'" />
      <img src="../assets/dog.jpg" alt="dog" v-else-if="animal === 'dog'" />
      <img src="../assets/cat.jpg" alt="cat" v-else-if="animal === 'cat'" />
      <p v-else>Choose an Animal...</p>
    </div>
    <p>Do You Like...</p>
    <div class="btn-container">
      <button @click="animal = 'bird'" class="btn btn-success me-2">Birds</button>
      <button @click="animal = 'dog'" class="btn btn-success me-2">Dogs</button>
      <button @click="animal = 'cat'" class="btn btn-success">Cats</button>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'

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
