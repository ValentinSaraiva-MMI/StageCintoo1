<script setup>
import {
  onBeforeMount,
  onBeforeUnmount,
  onBeforeUpdate,
  onMounted,
  onUnmounted,
  onUpdated,
  ref
} from 'vue'

let count = ref(0)

onBeforeMount(() => {
  console.log('onBeforeMount')
})

onMounted(() => {
  console.log('onMounted')
  alert('Bonjour')
})

onBeforeUpdate(() => {
  console.log('onBeforeUpdate')
})
onUpdated(() => {
  console.log('onUpdated')
})

onBeforeUnmount(() => {
  alert('au revoir')
})

onUnmounted(() => {
  console.log('onUnmounted')
})
</script>

<template>
  <div>
    <button @click="count++">count ={{ count }}</button>
  </div>
</template>

<style scoped></style>
