<script>
export default {
  data() {
	  return {
    	counter: 0
  	}
	},
  methods: {
    incrementCounter(event) {
      // recebe automaticamente o objeto DOM Event nativo 
      alert(event);
      this.counter++;
    }
	}
}
</script>

<template>
  <!--
 		@click -> Manipuladores embutidos
    incrementCounter -> Manipuladores de método
  -->
	<button @click="incrementCounter">Add 1</button>
	<p>The button above has been clicked {{ counter }} times.</p>
</template>
