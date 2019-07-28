<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <SigPlot id="plot1">
      <ArrayLayer data="[1,2,3,4,5]" />
    </SigPlot>
  </div>
</template>

<script>
import SigPlot from './components/SigPlot.vue'
import ArrayLayer from './components/ArrayLayer.vue'

export default {
  name: 'app',
  components: {
    SigPlot,
    ArrayLayer,
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

#plot1 {
  height: 500px;
  width: 500px;
}

</style>
