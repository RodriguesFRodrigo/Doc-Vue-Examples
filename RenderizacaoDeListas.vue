<script setup>
import { ref } from 'vue'
const parentMsg = ref('Parent')
const list = ref([{message: 'Foo'}, {message: 'Bar'}])
const myObject = ref({
	title: 'How to do lists in Vue',
  author: 'Jane Doe',
  publishedAt: '2016-04-10'
})
</script>

<template>
  <h2>
    v-for com arrays
  </h2>
  <li v-for="(item, index) in list">{{ parentMsg }} - {{ index }} - {{ item.message }}</li>
  
  <!-- Podemos usar desestruturação -->
  <li v-for="({message}, index) of list">{{ parentMsg }} - {{ index }} - {{ message }}</li>
  
  <h2>
    v-for com objetos
  </h2>
  <!-- v-for com objetos -->
  <!-- ordem de iteração será baseada no resultado da chamada Object.keys()do objeto [''title'', ''author'', ''publishedAt'']-->
  <li v-for="(value, key, index) of myObject">{{ index }}. {{ key }}: {{ value }}</li>
  
  <h2>
    v-for com inteiros
  </h2>
  <p v-for="n in 4">Internacional 4 x 0 São Luiz</p>
  
  <h2>
    v-for com template
  </h2>
  <ul>
    <template v-for="item in list">
    	<li>{{ item.message }}</li>
    </template>
  </ul>
  
  <h2>
    Mantendo o estado com key
  </h2>
  <!-- Ao usar <template v-for>, o key deve ser colocado no <template> contêiner: -->
  <template v-for="item in list" :key="item.message">
    <p>
      {{ item.message }}
    </p>
  </template>
</template>
