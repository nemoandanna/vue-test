<template>
  <div id="app">
    <time-hmoe></time-hmoe>
    <!-- <router-view/> -->
  </div>
</template>

<script>
import Timehome from './components/pages/home/timehome'

export default {
  name: 'App',
  components:{
    'time-hmoe':Timehome
    

  }
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
  background: #d8d8d8;
}
</style>
