<template>
  <div id="app">
    <RestaurantRow v-for="(row, index) in 6" :key="index"/>   
  </div>
</template>

<script>
import RestaurantRow from './components/RestaurantRow.vue'

export default {
  name: 'App',
  components: {
    RestaurantRow,    
  }
}
</script>

<style>
@import url('./style/reset.css');
@import url('./style/roboto.css');
#app {
  font-family: 'Roboto', sans-serif;
  padding: 20px;
}
</style>
