<template>
  <div id="app">
    <Fib msg="Fibonacci Sequence"/>  <!-- Sends the message to the component, Fib.vue.-->
  </div>
</template>

<script>
import Fib from './components/Fib.vue'

export default {
  name: 'App',
  components: {
    Fib
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
