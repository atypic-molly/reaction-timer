<template>
  <h1>Ninja Reaction Timer</h1>
  <button @click="start">play</button>
</template>

<!--data is an object that returns functions-->
<script>
export default {
  name: 'App',
  components: { },
  
  data() {
    return {
      isPLaying: false,
      delay: null
    }
  },
  methods: {
    start() {
      this.delay = 2000 + Math.random() * 5000
      this.isPLaying = true
      console.log(this.delay)
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
  color: #444;
  margin-top: 60px;
}
</style>
