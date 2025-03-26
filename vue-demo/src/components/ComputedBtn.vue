<template>
  <div>
    <h1>Does {{ user.name }} have tasks to do?</h1>
    <h2>{{ yesNo }}</h2>
  </div>
</template>

<script setup>
import { reactive, computed } from 'vue'

const user = reactive({
  name: 'Kayson Souksaly',
  tasks: ['1. Learn vue', '2. Play game', '3. Sleep'],
})

const yesNo = computed(() => {
  return user.tasks.length > 0 ? 'Yes' : 'No'
})
</script>
