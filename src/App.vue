<template>
  <h1>Ninja Reaction Timer</h1>
  <button @click="start">play</button>
  <Block v-if="isPLaying" :delay="delay" />
</template>

<!--data is an object that returns functions-->
<script>
import Block from './components/Block.vue'
export default {
  name: 'App',
  components: { Block },
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
