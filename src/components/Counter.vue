<template>
  <div class="counter">
    <h1>{{ counter }}</h1>
    <h2>{{ counter }} x 2 = {{ counterMultiplied() }}</h2>
  </div>
  <div class="buttons">
    <button @click="decrease">-</button>
    <button @click="increase">+</button>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'Counter',

  data() {
    return {
      counter: 0
    }
  },
  props: {
    msg: String,
  },
  methods: {
    decrease() {
      this.counter--;
    },
    increase() {
      this.counter++;
    },
    counterMultiplied() {
      return this.counter * 2
    }
  }
});
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.counter h1 {
  font-size: 80px;
}

.counter

.buttons {
  margin-top: 20px;
}

.buttons button {
  font-size: 40px;
  width: 100px;
}

.buttons button:first-child {
  margin-right: 10px;
}
</style>
