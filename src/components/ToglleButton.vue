<script setup>
import { ref } from 'vue'

const Ligth = ref(true)

function toggle() {
  Ligth.value=!Ligth.value
}
</script>

<template>
  <button @click="toggle">alternar</button>
  <h1 v-if="Ligth">Turn On</h1>
  <h1 v-else>Turn Off</h1>
</template>