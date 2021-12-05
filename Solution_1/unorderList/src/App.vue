<template>
<h3>Cycle through the numbers 3 – 103</h3>
  <UnorderList/>
</template>

<script>
import UnorderList from './components/UnorderList'

export default {
  name: 'App',
  components: {
    UnorderList
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
