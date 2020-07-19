<template>
  <div id="app">
    <trial-pack/>
  </div>
</template>

<script>
import TrialPack from './components/TrialPack.vue';

export default {
  name: 'App',
  components: {
    TrialPack
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
