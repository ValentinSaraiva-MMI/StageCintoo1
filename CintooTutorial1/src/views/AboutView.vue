<script setup>
import { ref } from 'vue'

const test = ref('')

const items = ref([
  { id: 1, text: 'test' },
  { id: 2, text: 'test2' },
  { id: 3, text: 'test3' }
])

const flavors = ref([
  { id: 1, text: 'chocolat' },
  { id: 2, text: 'vanille' },
  { id: 3, text: 'pistcahe' },
  { id: 4, text: 'bangarang' }
])

console.log(flavors)

const newitem = ref('')

const newItemPriority = ref('low')
const newHighItemPriority = ref('false')

const flavorsArray = ref([])
</script>

<template>
  <div>
    <div class="about">
      <ul>
        <li v-for="({ id, text }, index) in items" :key="id">
          {{ text }}
        </li>
      </ul>
    </div>

    <input v-model="newitem" type="text" placeholder="text" />

    <label>
      <input type="radio" v-model="newItemPriority" value="low" />
      low
    </label>
    <label>
      <input type="radio" v-model="newItemPriority" value="High" />
      High
    </label>

    <label>
      <input type="checkbox" v-model="flavorsArray" value="banane" />
      banane
    </label>
    <label>
      <input type="checkbox" v-model="flavorsArray" value="vanille" />
      Vanille
    </label>
    <label>
      <input type="checkbox" v-model="flavorsArray" value="Chocolat" />
      Chocolat
    </label>

    <p>{{ newitem }}</p>
    <p>{{ newItemPriority }}</p>
    <p>{{ flavorsArray }}</p>

    <input type="checkbox" v-model="newHighItemPriority" />
    <p>{{ newHighItemPriority }}</p>

    <div v-if="newHighItemPriority == true">
      <p>test</p>
    </div>

    <div v-else>test2</div>

    <ul>
      <li v-for="({ id, text }, index) in flavors" :key="id">
        {{ index }}
        {{ text }}
      </li>
    </ul>

    <div>
      <input v-model="test" type="text" placeholder="text" />

      <p>{{ test }}</p>
    </div>
  </div>
</template>

<style>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}
</style>
