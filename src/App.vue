<template>
  <div id="app">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <HelloWorld1>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import HelloWorld1 from './components/Cercle.vue'

export default {
  name: 'App',
  components: {
    HelloWorld,
    HelloWorld1
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
