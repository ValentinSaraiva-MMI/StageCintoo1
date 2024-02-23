<script setup>
import { ref } from 'vue'

// give each todo a unique id
let id = 0

const todos = ref([
  { id: id++, text: 'Learn HTML' },
  { id: id++, text: 'Learn JavaScript' },
  { id: id++, text: 'Learn Vue' }
])

let lastid = ref(todos.value[todos.value.length - 1].id)

function giveId() {
  console.log(lastid)
}
function giveTodos() {
  console.log(todos)
}

let newTodo = {
  id: id++,
  text: ''
}

function addTodo() {
  todos.value.push(newTodo)

  newTodo = { id: id++, text: '' }
}

function removeTodo(todo) {
  todos.value = todos.value.filter((t) => t !== todo)
}

// let array = ['a', 'b', 'c', 'd', 'e'] // Exemple de tableau
// let index = 1 // L'index de l'élément à supprimer (0-based index)
// array.splice(index, 1)
// console.log(array) // ['a', 'b', 'd', 'e']
</script>

<template>
  <div>
    <button @click="giveId()">giveId</button>
    <button @click="giveTodos()">giveTodos</button>
    <p>{{ todos }}</p>

    <form @submit.prevent="addTodo">
      <input v-model="newTodo.text" />
      <button>Add Todo</button>
    </form>

    <ul>
      <li v-for="todo in todos" :key="todo.id">
        {{ todo.text }}
        <button :id="todo.id" @click="removeTodo(todo)">X</button>
      </li>
    </ul>
  </div>
</template>
