<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <h1>{{ add(100, num) }}</h1>
  <h1>{{ mul(120) }}</h1>
</template>

<script>

export default {
  name: 'App',
  data() {
    return {
      num: 10,
    }
  },
  methods: {
    add(a, b) {
      return a + b
    },
    mul(a) {
      return a * this.num;
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
