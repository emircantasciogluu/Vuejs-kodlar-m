<script setup lang="ts">
import {ref} from 'vue';

const members = ref(["Emir", "Mehmet", "Ahmet"])

const member = ref({
  name: "Batu",
  age: 30,
  city: 'Rize'
})


</script>

<template>
  <div> <!--Array-->
    <ul>
      <li v-for="member in members" :key="member">
        {{ member }}
      </li>
    </ul>
  </div>

  <div> <!--Object-->
    <ul>
      <li v-for="(key, value) in member" :key="value">
      {{ value }} - {{ key }}</li>
    </ul>
  </div>
</template>

<style>
ul{
  font-size: 30px;
  margin-top: 100px;
}


</style>
