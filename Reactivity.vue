<script setup lang="ts">

import {computed, ref, watch} from 'vue';

const count = ref(0)
const log = ref<string>()

function updateCount(){
  count.value++
}

watch(count, (newValue, oldValue)=>{
  log.value = `oldValue: ${oldValue} - newValue: ${newValue}`
})

const countViewModel = computed(()=> {
  return count.value + ' kalem'
})

</script>

<template>
  <div>
    <button @click="updateCount">{{ countViewModel }}</button>
    <pre>
      {{ log }}
    </pre>
  </div>
</template>

<style>

button{
  font-size: 30px;
  margin-top: 100px;
}

</style>
