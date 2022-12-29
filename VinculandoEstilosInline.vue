<script setup>
import { ref } from 'vue'
import { reactive } from 'vue'
  
const msg = ref('Hello World!');
const activeColor = ref('red');
const fontSize = ref(30);

const styleObject = reactive({
 	color: 'red',
  fontSize: '13px'
})

</script>

<template>
  <h1 :style="{color: activeColor, fontSize: fontSize + 'px'}">{{ msg }}</h1>
  <!-- using object -->
  <h1 :style="styleObject">{{ msg }}</h1>
  <input v-model="msg">
</template>
