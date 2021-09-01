<template>
  <div id="app">
    <IndexComponent />
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import IndexComponent from './components/IndexComponent.vue'

export default {
  name: 'App',
  components: {
    IndexComponent
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
