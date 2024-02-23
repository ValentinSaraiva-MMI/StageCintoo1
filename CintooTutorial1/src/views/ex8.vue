<script setup>
import { onMounted, ref } from 'vue'

const pElementRef = ref(null)
const pElementRef2 = ref(null)
let change = ref(false)

function ischecked() {
  change.value = !change.value
  console.log(change.value)
}

onMounted(() => {
  pElementRef.value.textContent = 'changed'
})

function test() {
  if (change.value == true) {
    pElementRef2.value.textContent = 'changed'
  } else {
    pElementRef2.value.textContent = 'normal'
  }

  change.value = !change.value
}
</script>

<template>
  <div>
    <p ref="pElementRef">Hello</p>
    <p ref="pElementRef2">Ref2</p>

    <button @click="ischecked">Change vallue</button>
    <button @click="test">Change vallue</button>
  </div>
</template>
