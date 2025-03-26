<template>
  <div class="list-box">
    <ul class="list-unstyled">
      <li v-for="(todo, index) in toDoList.list" :key="index">{{ index + 1 }}. {{ todo }}</li>
    </ul>
  </div>
</template>

<script setup>
import { reactive } from 'vue'

const toDoList = reactive({
  list: ['Throw garbage', 'Clean room', 'Go to work', 'Finish assignment'],
})
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
