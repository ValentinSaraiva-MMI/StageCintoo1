<script setup>
import ChildComp3 from '@/components/ChildComp3.vue'

import JSConfetti from 'js-confetti'

const confetti = new JSConfetti()

function showConfetti() {
  confetti.addConfetti()
}

showConfetti()
</script>

<template>
  <p>ex12</p>
  <button @click="showConfetti">GG</button>
  <ChildComp3 @click="showConfetti">Hey je passe du contenu dans le slot 👏</ChildComp3>
  <br />
  <ChildComp3> </ChildComp3>
</template>

<style scoped></style>
