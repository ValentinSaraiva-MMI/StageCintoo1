<script setup>
const props = defineProps({
  msg: String
})
</script>

<template>
  <h1 style="color: red">{{ msg }}</h1>
</template>

<style scoped></style>
