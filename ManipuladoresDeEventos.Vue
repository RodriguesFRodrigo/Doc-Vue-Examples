<script>
export default {
  data() {
    return {
      counter: 0,
      name: 'Vue.js'
    }
  },
  methods: {
    greet(event) {
      // `this` inside methods points to the current active instance
      alert(`Hello ${this.name}!`);
      // `event` is the native DOM event
      if (event) {
        alert(event.target.tagName);
      }
    },
    sayHello(name) {
      alert(`Hello ${name}`);
    },
    war(message, event) {
      alert(event);
    }
  },
}
</script>

<template>
  <h1>Counter has value: {{ counter }}</h1>
  <!-- inline handles -->
  <div>
    <button @click="counter++">Increment</button>
  </div>
  <div>
    <button @click="greet">Greet</button>    
  </div>
  <div>
    <button @click="sayHello('Rodrigo', event)">Say Hello</button>    
  </div>
  <!-- Accessing Event Argument in Inline Handlers -->
  <button @click="war('Danger!', $event)">Say Warn</button>
  <button @click="(event) => war('Danger!', event)">Say Warn</button>
</template>

