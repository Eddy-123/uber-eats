<template>
  <div id="app">
    <HomeLand/>
  </div>
</template>

<script>
import HomeLand from './page/homeLand.vue'

export default {
  name: 'App',
  components: {
    HomeLand    
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
