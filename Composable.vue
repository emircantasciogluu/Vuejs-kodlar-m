<script setup lang="ts">
import { reactive } from 'vue';
import {ref} from 'vue'

const breakPoints = reactive({
  sm: false,
  md: false,
  lg: false
})
const width = ref(window.innerWidth)

window.addEventListener("resize", function(){
  const currentWindowWidth = window.innerWidth
  width.value = currentWindowWidth

  breakPoints.sm = currentWindowWidth <= 800
  breakPoints.md = currentWindowWidth > 800 && currentWindowWidth <=1200
  breakPoints.lg = currentWindowWidth > 1200

})

</script>

<template>
  <div v-if="breakPoints.sm">Small Screen</div>
  <div v-if="breakPoints.md">Medium Screen</div>
  <div v-if="breakPoints.lg">Large Screen</div>
  <h1>{{ width }}</h1>
</template>

<style>
div{
  font-size: 50px;
}


</style>

