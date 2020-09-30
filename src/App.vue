<template>
  <div id="app">
    <Launcher/>
  </div>
</template>

<script>
import Launcher from './components/Launcher'

export default {
  name: 'App',
  components: {
    Launcher
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

}
</style>
