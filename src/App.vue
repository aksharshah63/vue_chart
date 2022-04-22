<template>
  <div id="app">
    <div class="container">
      <div class="row">
        <div class="col-lg-6">
          <h5 class="text-center">Population with Biomechanics</h5>
          <PieChart />
        </div>
        <div class="col-lg-6">
          <h5 class="text-center">Population with Cardio</h5>
          <PieChart2 />
        </div>
      </div>
      <div class="row">
        <div class="col-lg-4">
          <h5 class="text-center">Cardio Score by Age</h5>
          <BarChart />
        </div>
        <div class="col-lg-4">
          <h5 class="text-center">Cardio Score by Cluster</h5>
          <BarChart2 />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import BarChart from './components/BarChart.vue'
import PieChart from './components/PieChart.vue'
import PieChart2 from './components/PieChart2.vue'
import BarChart2 from './components/BarChart2.vue'

export default {
  name: 'App',
  components: 
  { 
    BarChart,
    PieChart,
    PieChart2,
    BarChart2
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
