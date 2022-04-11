<template>
  <div id="app">
    <RestaurantCard/>    
  </div>
</template>

<script>
import RestaurantCard from './components/RestaurantCard.vue'
export default {
  name: 'App',
  components: {
    RestaurantCard
  }
}
</script>

<style>
@import url('./style/reset.css');
@import url('./style/roboto.css');
#app {
  font-family: 'Roboto', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
