<script setup>
import { ref } from 'vue'

const msg = ref('Hello World!')
const awesome = ref(false);
const type = ref('C');
const ok = ref(true);
  
</script>

<template>
  <button @click="awesome = !awesome">Toggle</button>
  <h1 v-if="awesome">Vue is awesome!</h1>
  <h1 v-else>Oh no 😢</h1>
  <p v-if="type === 'A'">A</p>
  <p v-else-if="type === 'B'">B</p>
  <p v-else>C</p>
  
  <template v-if="ok">
  	<h1>GYM</h1>
    <p>Army and Chester</p>
  </template>
  
  <h1 v-show="ok">Hello!</h1>

  
</template>
