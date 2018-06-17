<template>
  <div id="app">
    <img src="./assets/logo.png">
    <buttonComp username="Tzahi" :click="click" msg="Tzahi's context-menu"></buttonComp>
    <menu :click="click" isFolder = false></menu>
  </div>
</template>

<script>
import mymenu from "./components/menu.vue";
import buttonComp from './components/buttonComp.vue'

export default {
  name: 'app',
  components: {
    buttonComp,
    mymenu
  },
  data(){
    return{
      click: false,
    }
  },
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
