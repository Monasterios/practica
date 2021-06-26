<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <Abuelo msg="Hola desde Abuelo"/>
</template>

<script>
import Abuelo from './components/Abuelo.vue'

export default {
  name: 'App',
  components: {
    Abuelo
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
