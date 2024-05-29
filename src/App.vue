<template>
  <img class="logo" alt="InterArk Logo" src="./assets/InterArk.jpg">
  <HelloWorld msg="ようこそ"/>
  <div><TodayExample/></div>
  <div><ToglleButton/></div>
  <div><GraphsAmcharts/></div>

</template>

<script>
import HelloWorld from './components/HelloWorld.vue';
import TodayExample from './components/TodayExample.vue';
import ToglleButton from './components/ToglleButton.vue';
import GraphsAmcharts from './components/GraphsAmcharts.vue';

export default {
  name: 'App',
  components: {
    HelloWorld,
    TodayExample,
    ToglleButton,
    GraphsAmcharts
    
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

.logo {
  height: 120px;
  
}
</style> 
