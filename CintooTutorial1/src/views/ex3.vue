<script setup>
import { ref } from 'vue'

const count = ref(0)

function increment() {
  console.log(count.value++)
}
count
</script>

<template>
  <!-- make this button work -->
  <button @click="increment">count is: {{ count }}</button>
</template>
