<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <Nav></Nav>
    <Onlinefriends/>
  </div>
</template>

<script>
import Nav from './components/Nav.vue'
import Onlinefriends from './components/Onlinefriends.vue'

export default {
  name: 'App',
  data(){
      return{
        
      }
  },
  components: {
    Nav,Onlinefriends
  },
  methods: {
    
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
