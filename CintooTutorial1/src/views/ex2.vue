<script setup>
import { ref } from 'vue'

const titleClass = ref('title')
const id = 'id1'
</script>

<template>
  <h1 :class="titleClass" :id="id">Make me red</h1>
  <!-- add dynamic class binding here -->
</template>

<style>
.title {
  color: red;
}
</style>
