<template>
<div>
  <img alt="Vue logo" src="./assets/logo.png">
  <!--<HelloWorld msg="Welcome to Your Vue.js App"/> -->
  <databind />
  </div>
</template>

<script>
//import HelloWorld from './components/HelloWorld.vue'

//import home from './components/Home.vue'

import databind from './components/databinding.vue'
export default {
  name: 'App',
  components: {
   // HelloWorld,
    databind
    
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
