<template>
  <div id="app">
    <h1>Vuex Counter</h1>
    <p>Count: {{ count }}</p>
    <p>Double Count: {{ doubleCount }}</p>
    <button @click="increment">Increment</button>
    <button @click="decrement">Decrement</button>
  </div>
</template>

<script>
import { mapState, mapGetters, mapActions } from 'vuex';

export default {
  computed: {
    ...mapState(['count']),
    ...mapGetters(['doubleCount']),
  },
  methods: {
    ...mapActions(['increment', 'decrement']),
  },
};
</script>

<style>
#app {
  text-align: center;
  margin-top: 40px;
}

button {
  margin: 5px;
}
</style>
