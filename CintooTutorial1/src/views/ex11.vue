<script setup>
import { ref } from 'vue'
import ChildComp2 from '@/components/ChildComp2.vue'
</script>

<template>
  <div>
    <ChildComp2 @response="(msg) => (childMsg = msg)" />
    <p>test</p>
  </div>
</template>

<style scoped></style>
