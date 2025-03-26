<template>
  <div>
    <img src="../assets/codeImage/listRenderCode1.png" alt="v-for Code Block" class="mb-5" />
    <img src="../assets/codeImage/listRenderCode2.png" alt="v-for Code Block" class="mb-5" />

    <h1 class="text-danger">Code Example</h1>
    <input
      v-model="newItem"
      @keyup.enter="addItem"
      type="text"
      placeholder="Add a new task..."
      class="form-control mb-3 w-50 mx-auto"
    />

    <!-- Button to add the task manually -->
    <button @click="addItem" class="btn btn-success mb-4">Add</button>

    <h2>My todo List</h2>
    <div class="list-box">
      <ul class="list-unstyled">
        <!-- Render each todo item using v-for -->
        <!-- The index is used to number the items and also as a unique key -->
        <li v-for="(todo, index) in toDoList.list" :key="index">{{ index + 1 }}. {{ todo }}</li>
      </ul>
    </div>
  </div>
</template>

<script setup>
// Import reactive to create a reactive object
import { reactive, ref } from 'vue'

// Create a reactive object that contains a list of to-do items
const toDoList = reactive({
  list: ['Throw garbage', 'Clean room'],
})

// Ref for the input field
const newItem = ref('')

function addItem() {
  if (newItem.value.trim() !== '') {
    toDoList.list.push(newItem.value.trim())
    newItem.value = ''
  }
}
</script>

<style scoped>
.list-box {
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: left;
}
</style>
