<template>
  <div>
    <img src="../assets/codeImage/reactiveCode1.png" alt="Reactive Code Block" class="mb-5" />
    <img src="../assets/codeImage/reactiveCode2.png" alt="Reactive Code Block" class="mb-5" />

    <h1 class="text-danger">Code Example</h1>
    <h1>user information:</h1>

    <div class="box">
      <div class="user-info">
        <p>Full Name: {{ fullName }}</p>
        <p>Age: {{ age }}</p>
        <p>Hobby: {{ hobby }}</p>
      </div>
    </div>

    <button @click="updateUserInformation()" class="btn btn-success">Click Me!</button>
  </div>
</template>

<script setup>
import { reactive, ref } from 'vue'

// Create a reactive object to store user details
const userInformation = reactive({
  firstName: 'Jack',
  lastName: 'smith',
  age: 21,
  hobby: 'Cooking',
})

// Define refs to hold and display extracted values from the reactive object
const fullName = ref()
const age = ref()
const hobby = ref()

// Populate the refs using values from the reactive object when button is clicked
function updateUserInformation() {
  fullName.value = userInformation.firstName + ' ' + userInformation.lastName
  age.value = userInformation.age
  hobby.value = userInformation.hobby
}
</script>

<style scoped>
p {
  text-align: start;
}

.box {
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
}

.user-info {
  width: 20vw;
}
</style>
