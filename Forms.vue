<script>
export default {
  data() {
    return {
      text1: '',
      text2: '',
      text3: '',
      checked: '',
      checkedNames: [],
      picked: '',
    }
  }
}
</script>

<template>
  <!-- Native -->
  <div>
    <p>
      Text has the value: {{ text1 }}
    </p>
  	<input
    	:value="text1"
    	@input="event => text1 = event.target.value"
  	/>
  </div>
  
  <!-- Usando v-model -->
  <div>
    <p>
      Text has the value: {{ text2 }}
    </p>
  	<input v-model="text2"/>
  </div>
  
  <div>
    <p>
      The textarea has the value: {{ text3 }}
    </p>
    <textarea v-model="text3"></textarea>
  </div>
  
  <div>
  	<input type="checkbox" id="checkbox" v-model="checked" />
		<label for="checkbox">{{ checked }}</label>
    <div>Checked names: {{ checkedNames }}</div>
    <input type="checkbox" id="jack" value="Jack" v-model="checkedNames">
		<label for="jack">Jack</label>
		<input type="checkbox" id="john" value="John" v-model="checkedNames">
		<label for="john">John</label>
		<input type="checkbox" id="mike" value="Mike" v-model="checkedNames">
		<label for="mike">Mike</label>
  </div>
  
  <div>
    <div>Picked: {{ picked }}</div>
    <input type="radio" id="one" value="One" v-model="picked" />
    <label for="one">One</label>
    <input type="radio" id="two" value="Two" v-model="picked" />
    <label for="two">Two</label>
  </div>
</template>
