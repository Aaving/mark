<template>
  <div id="app">
    <Top/>
    <List/>
  </div>
</template>

<script>

import Top from './components/Top.vue'
import List from './components/List.vue'
export default {
  name: 'App',
  components: {Top,List},
  data(){
    return {
      list:[
        []
      ]
    }
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
