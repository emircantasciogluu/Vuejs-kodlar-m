<script setup lang="ts">
import { ref } from 'vue'
const name = ref()
const txtName = ref()
const check = ref()
</script>

<template>
  <div>
    <input type="text" v-model="name">
    <h1>{{ name }}</h1>
  </div>

  <div>
    <textarea v-model="txtName"></textarea>
    <pre>{{ txtName }}</pre>
  </div>

  <div>
    <label >
      <input type="checkbox" v-model="check">
      ben bir checkboxum
    </label>
    <p>{{ check }}</p>
  </div>
</template>

<style>
input{
  font-size: 30px;
  margin-top: 100px;
  border: 2px solid #c0c0c0;
}
textarea{
  font-size: 30px;
  margin-top: 100px;
  border: 2px solid #c0c0c0;
}


</style>
