<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
    <!-- <h2>Consumiendo api rando user</h2> -->
    <!-- <Imagenes/> -->
    <hr><br>
    <router-link to="/" class="btn btn-primary">Home</router-link>
    <router-link to="/imagenes" class="btn btn-info">Images</router-link>
    <router-link to="/yo" class="btn btn-warning">About me</router-link>
    <br><br><hr>
    <router-view></router-view>
  </div>
</template>

<script>
// import Imagenes from './components/Imagenes.vue'

export default {
  name: 'app',
  // components: {
  //   Imagenes
  // }
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
.btn{
  padding: 8px;
  margin: 5px;
  border-radius: 4px;
  box-shadow:0px 2px 3px black;
  text-decoration: none;
  transition: all .4s;
  color: black;
}
.btn:hover{
  background: teal;
}
</style>
