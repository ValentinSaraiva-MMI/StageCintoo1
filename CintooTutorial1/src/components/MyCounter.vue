<script setup>
import { ref } from 'vue'

let counter = ref(0)
let test = ref(0)
</script>

<template>
  <div>
    <button @click="counter++, test++">Current count = {{ counter }}</button>
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
