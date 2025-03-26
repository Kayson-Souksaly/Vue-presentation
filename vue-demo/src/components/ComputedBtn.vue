<template>
  <div>
    <img src="../assets/codeImage/computedCode2.png" alt="Computed Code Block" class="mb-5" />
    <img src="../assets/codeImage/computedCode.png" alt="Computed Code Block" class="mb-5" />

    <h1 class="text-danger">Code Example</h1>
    <h1>Does {{ user.name }} have tasks to do?</h1>
    <div class="list-box">
      <ul>
        <li v-for="(userInfo, index) in user.tasks" :key="index">
          {{ userInfo }}
        </li>
      </ul>
    </div>

    <!-- Call the computed state -->
    <h2>{{ yesNo }}</h2>

    <!-- Delete the items in the user.task array -->
    <button class="btn btn-success" @click="user.tasks = []">Delete List</button>
  </div>
</template>

<script setup>
import { reactive, computed } from 'vue'

// Create a reactive object with a name and an array of tasks
const user = reactive({
  name: 'Kayson Souksaly',
  tasks: ['Learn vue', 'Play game', 'Sleep'],
})

// Computed property returns 'Yes' if the user has tasks, otherwise 'No'
const yesNo = computed(() => {
  return user.tasks.length > 0 ? 'Yes' : 'No'
})
</script>

<style scoped>
.list-box {
  height: 20vh;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: left;
}
</style>
