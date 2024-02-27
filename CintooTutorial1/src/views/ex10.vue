<script setup>
import { ref } from 'vue'
import ChildComp from '../components/ChildComp.vue'

const greeting = ref('Hello from parent')
</script>

<template>
  <ChildComp msg="Ceci est un message de props" msg2="Props2"></ChildComp>
</template>
