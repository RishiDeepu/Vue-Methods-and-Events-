<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <h1>{{ add(100, num) }}</h1>
  <h1>{{ mul(120) }}</h1>
  <div class="a">
    <h1 class="b">{{ name }}</h1>
    <button @click="changeName(), inc()">fullname</button>
  </div>
  <div class="secondDiv">
    <h1 class="c">{{ counter }}</h1>
    <button v-on:click="inc()">Increment</button>
    <button v-on:click="dec($event)">Decrement</button>
    <button v-on:click="preset()">Set To Zero</button>
    <button @click="set($event)">Set To 100</button>

  </div>
</template>

<script>

export default {
  name: 'App',
  data() {
    return {
      num: 10,
      name: "Rishi",
      fullName: "Rishikesh",
      counter: 0
    }
  },
  methods: {
    changeName() {
      console.log("this.fullName", this.fullName);
      return this.name = this.fullName
    },
    add(a, b) {
      return a + b
    },
    mul(a) {
      return a * this.num;
    },
    inc() {
      return this.counter++
    },
    dec(event) {
      console.log("event", event);
      return this.counter--
    },
    preset() {
      return this.counter = 0
    },
    set(event) {
      console.log("event", event);
      return this.counter = 100

    },

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

.a {
  background-color: black;
  color: white;
  width: 600px;
  height: 100px;
  margin-left: 380px;
}

.b {
  padding: 6px;
}

.secondDiv {
  background-color: black;
  color: white;
  width: 600px;
  height: 100px;
  margin-left: 380px;

}

.c {
  padding: 6px;
}
</style>
