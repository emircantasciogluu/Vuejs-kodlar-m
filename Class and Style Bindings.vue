<script setup lang="ts">
import { ref } from 'vue'

const isRed = ref(false)
const myStyle = ref({
  color: 'blue',
  background: 'red',
  padding: '12px 24px' 
}
)

</script>

<template>
  <div class="container">
    <h1 :class="{ baslik: isRed }">Emir Can Taşcıoğlu</h1>
    <h1 :style="myStyle">Vue.js Öğreniyorum</h1>
    <button @click="isRed = true">change color</button>
    <button @click=" myStyle.background = 'yellow' ">Change Bg</button>
  </div>
</template>

<style>
.baslik{
  color: red;
}



</style>
