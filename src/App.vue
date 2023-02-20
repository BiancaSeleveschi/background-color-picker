<template>
  <div id="app">
    <h1>Change the color</h1>
    <button @click="generator" class="btn btn-light border-2 rounded-2 p-2 shadow m-3">New color</button>
    <h3>{{ color }}</h3>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      color: "#FFFFFF"
    };
  },
  methods: {
    generator: function () {
      this.color = '#' + (Math.random() * 0xFFFFFF << 0).toString(16);
      document.body.style.background = this.color;
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
