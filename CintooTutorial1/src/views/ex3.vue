<script setup>
import { ref } from 'vue'

let count = ref(0)

function increment() {
  count.value++
  console.log(count)
}
</script>

<template>
  <!-- make this button work -->
  <button @click="increment">count is: {{ count }}</button>
</template>
