<template>
  <div>
    <h1>user information:</h1>
    <div class="box">
      <p>Full Name: {{ fullName }}</p>
      <p>Age: {{ age }}</p>
      <p>Hobby: {{ hobby }}</p>
    </div>

    <button @click="updateUserInformation()" class="btn btn-success">Click Me!</button>
  </div>
</template>

<script setup>
import { reactive, ref } from 'vue'

const userInformation = reactive({
  firstName: 'Jack',
  lastName: 'smith',
  age: 21,
  hobby: 'Cooking',
})

const fullName = ref()
const age = ref()
const hobby = ref()

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
</style>
