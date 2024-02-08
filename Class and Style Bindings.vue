<script setup lang="ts">
import { ref } from 'vue'
const isRed = ref(false)



</script>

<template>
  <div class="container">
    <h1 :class="{ baslik: isRed }">Emir Can Taşcıoğlu</h1>
    <button @click="isRed = true">change color</button>
    <button @click="isRed = false">Reset</button>
  </div>
</template>

<style>
.baslik{
  color: red;
}



</style>
