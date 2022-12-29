<script setup>
import { ref } from 'vue'

const msg = ref('Hello World!');
const isActive = ref('active');
const isOutline = ref('outline');
const isInputBold = ref(true);
</script>

<template>
  <h1 :class="[isActive, isOutline]">{{ msg }}</h1>
  <!-- verbose way -->
  <input v-model="msg" :class="[isInputBold ? 'bold' : '', isActive]">
  <!-- does not verbose way -->
  <input v-model="msg" :class="[{bold: isInputBold}, isActive]">
</template>

<style>
  .active {
    color: green;
  }
  
  .outline {
    border: 1px solid black;
  }
  
  .bold {
    font-weight: bold;
  }
</style>
