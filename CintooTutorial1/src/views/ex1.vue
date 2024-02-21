<script setup>
import { reactive, ref } from 'vue'

let counter = ref(0)
let message = reactive({ message1: 'Hello' })

console.log(message.message1)

function increment() {
  console.log(counter)
  counter.value++
}
</script>

<template>
  <div>
    <button @click="increment()">Current count = {{ counter }}</button>
    <div>
      <p class="superior" v-if="counter > 10">Counter is superior to 10</p>
      <p class="inferior" v-else>counter is inferior to 10</p>
    </div>
  </div>
</template>

<style scoped>
.superior {
  color: red;
}

.inferior {
  color: blue;
}
</style>
