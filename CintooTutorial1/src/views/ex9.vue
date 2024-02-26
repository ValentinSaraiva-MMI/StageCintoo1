<script setup>
import { ref, watch } from 'vue'

const todoId = ref(1)
const todoData = ref(null)

const count = ref(0)

watch(count, async (tkt) => {
  todoData.value = null // Efface les données précédentes

  try {
    const res = await fetch(`https://jsonplaceholder.typicode.com/todos/${count.value}`)
    const data = await res.json()
    todoData.value = data
  } catch (error) {
    console.error('Failed to fetch todo', error)
  }
})

/*

watch(count, async (tkt) => {
  todoData.value = null // Efface les données précédentes
  try {
    const res = await fetch(`https://jsonplaceholder.typicode.com/todos/${count.value}`)
    const data = await res.json() // Attend que les données JSON soient résolues
    todoData.value = data // Met à jour todoData avec les données JSON
  } catch (error) {
    console.error('Failed to fetch todo', error)
  }
})

*/
</script>

<template>
  <div>
    <p>Todo id: {{ todoId.value }}</p>
    <button @click="todoId.value++" :disabled="!todoData">Fetch next todo</button>
    <button @click="count++">count</button>
    <p v-if="!todoData">Loading...</p>
    <pre v-else>{{ todoData }}</pre>
  </div>
</template>
