<script setup>
const props = defineProps({ msg: String, msg2: String })
</script>

<template>
  <p>{{ msg }}</p>
  <h2>{{ msg2 }}</h2>
</template>

<style scoped></style>
