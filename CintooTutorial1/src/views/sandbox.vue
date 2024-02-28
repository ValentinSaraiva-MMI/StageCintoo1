<script setup>
import { ref, computed } from 'vue'

const values = ref([
  { id: 1, text: 'text1' },
  { id: 2, text: 'text2' },
  { id: 3, text: 'text3' }
])

const author = ref({
  name: 'Valentin Saraiva',
  books: ['titre1', 'titre2']
})

console.log(author.value.books)

const character = ref(0)

const title = ref('SandBox')
const yes = ref(true)
const text = ref('Ceci est chargé dynamiquement')
const titleClass = ref('red')
const test = ref(0)
const counter = ref(0)

console.log(titleClass.value)

function changecolor() {
  console.log(character.value.length)
  if (titleClass.value == 'red') {
    titleClass.value = 'green'
  } else {
    titleClass.value = 'red'
  }
}
</script>

<template>
  <button style="width: 100px" @click="yes = !yes">Wnt to show the first exercices ?</button>
  <div v-if="yes == true">
    <h1>{{ title }}</h1>
    <button style="width: 100px" @click="counter++">Value is : {{ counter }}</button>
    <p @click="changecolor()" v-bind:class="titleClass">{{ text }}</p>

    <p v-if="counter >= 3">test</p>

    <p v-if="titleClass == 'red'">RED</p>

    <p>Ceci est une liste de donnée dynamique</p>
    <ul>
      <li v-for="value in values" :key="value.id">
        {{ value.text }}
      </li>
    </ul>
  </div>

  <input v-model="character" type="text" placeholder="tape du text ici" />
  <p>{{ character.length }} /200</p>

  <span>{{ author.books.length > 0 ? 'yes' : 'no' }}</span>
</template>

<style scoped>
.red {
  color: red;
}

.green {
  color: green;
}
</style>
