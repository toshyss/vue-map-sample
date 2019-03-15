<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import 'leaflet/dist/leaflet.css';
import L from 'leaflet';

export default {
  // name: 'app',
  // components: {
  //   HelloWorld
  // }
  mounted() {
    L.map('app', { center:L.latLng( 35.6825, 139.752778 ), zoom:16 }).addLayer(
      L.tileLayer('http://{s}.tile.osm.org/{z}/{x}/{y}.png')
    )
  }
}
</script>

<style>
/* #app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
} */
html, body, #app { height: 100% }
body{ margin: 0 }
</style>
