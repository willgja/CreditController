<template>
  <div id="app">
    <MenuPrincipal/>
  </div>
</template>

<script>
import MenuPrincipal from './components/Menu.vue';


export default {
  name: 'App',
  components: {
    MenuPrincipal
    
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
