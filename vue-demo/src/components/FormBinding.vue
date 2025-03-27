<template>
  <div>
    <img src="../assets/codeImage/formEventCode1.png" alt="Form Event Code Block" class="mb-5" />
    <img src="../assets/codeImage/formEventCode2.png" alt="Form Event Code Block" class="mb-5" />

    <h1 class="text-danger">Code Example</h1>
    <h2>Solve this</h2>

    <!-- Display the math problem and show user's input -->
    <p>{{ num1 }} + {{ num2 }} = {{ userAnswer }}</p>

    <!-- Two-way binding: updates userAnswer on input -->
    <input
      v-model.number="userAnswer"
      @keyup.enter="calculate"
      type="number"
      placeholder="Add answer..."
      class="form-control mb-3 w-50 mx-auto"
    />

    <!-- Button also triggers answer checking -->
    <button @click="calculate" class="btn btn-success mb-4">Submit</button>

    <!-- Display result based on whether the answer is correct -->
    <div class="container w-100">
      <div class="result-box w-50">
        <h3 v-if="isAnswerCorrect == true" class="text-success">Correct!🥳</h3>
        <h3 v-else-if="isAnswerCorrect == false" class="text-danger">Incorrect!😥</h3>
        <h3 v-else class="text-info">Please answer!</h3>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'

// Generate two random numbers between 1–20
let num1 = ref(Math.floor(Math.random() * 20) + 1)
let num2 = ref(Math.floor(Math.random() * 20) + 1)

// Calculate their sum once
const sum = num1.value + num2.value

// Store user input and answer result
const userAnswer = ref('')
const isAnswerCorrect = ref()

// Compare user's answer to the correct sum
function calculate() {
  if (parseInt(userAnswer.value) == sum) {
    isAnswerCorrect.value = true
  } else {
    isAnswerCorrect.value = false
  }
}
</script>

<style scoped>
.container {
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>
