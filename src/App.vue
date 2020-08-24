<template>
  <div id="app">
    <StarWars v-if="result" :result="result"/>
  </div>
</template>

<script>
import StarWars from './components/StarWars';

export default {
  name: 'App',
  components: {
    StarWars
  },
  data: function() {
    return {
      result: {}
    }
  },
  mounted: function () {
    fetch('https://swapi.dev/api/people/1', { method : 'get'})
    .then(response => response.json()).then(resultData => {
      this.result = resultData;
    })
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
