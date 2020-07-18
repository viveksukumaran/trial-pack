<template>
  <div id="app">
    <!--<img alt="Vue logo" src="./assets/logo.png">    
    <HelloWorld msg="Welcome Vivek to Your Vue.js App"/>-->
    <trial-pack/>
  </div>
</template>

<script>
//import HelloWorld from './components/HelloWorld.vue';
import TrialPack from './components/TrialPack.vue';

export default {
  name: 'App',
  components: {
    //HelloWorld,
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
