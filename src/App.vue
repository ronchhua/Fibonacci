<template>
  <div id="app">
    <FibDisplay msg="Fibonacci Sequence"/>  <!-- Sends the message to the component, Fib.vue.-->
  </div>
</template>

<script>
import FibDisplay from './components/FibDisplay.vue'

export default {
  name: 'App',
  components: {
    FibDisplay
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
