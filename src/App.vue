<template>
  <div id="app">
    <RaiseToExp></RaiseToExp>
  </div>
</template>

<script>
import RaiseToExp from './components/RaiseToExp.vue'

export default {
  name: 'app',
  components: {
    RaiseToExp
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
}
</style>
