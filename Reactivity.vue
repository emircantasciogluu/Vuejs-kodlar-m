<script setup lang="ts">

import {ref, watch} from 'vue';

const count = ref(0)
const log = ref<string>()

function updateCount(){
  count.value++
}

watch(count, (newValue, oldValue)=>{
  log.value = `oldValue: ${oldValue} - newValue: ${newValue}`
})

</script>

<template>
  <div>
    <button @click="updateCount">{{ count }}</button>
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
