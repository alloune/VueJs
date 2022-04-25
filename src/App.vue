<template>

  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <helloWorld msg="Test de l'utilisation d'un props en plus"/>
  </div>
</template>

<script>

import helloWorld from "@/components/HelloWorld";
export default {
  name: 'App',
  components: {
    helloWorld,
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
