<template>
  <div id="app">
    <router-link to="/" tag="button">Accueil</router-link>
    <img alt="Vue logo" src="./assets/logo.png">
    <router-link to="/supplier" tag="button">liste des fournisseurs</router-link>
    <router-link to="/map" tag="button">Localisation fournisseurs</router-link>
    <router-view></router-view>
  </div>
</template>

<script>

export default {
  name: 'app'
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
