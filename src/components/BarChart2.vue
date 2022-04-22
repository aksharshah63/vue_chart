<template>
  <Bar :chart-data="chartData" :chart-options="chartOptions" :width="width" :height="height"/>
</template>

<script>
import { Bar } from 'vue-chartjs/legacy'
import { Chart as ChartJS, Title, Tooltip, Legend, BarElement, CategoryScale, LinearScale } from 'chart.js'

ChartJS.register(Title, Tooltip, Legend, BarElement, CategoryScale, LinearScale)

export default {
  name: 'BarChart',
  components: { Bar },
   props: {
    width: {
      type: Number,
      default: 400
    },
    height: {
      type: Number,
      default: 400
    },
  },
  data() {
    return {
      chartData: {
        labels: [ 'A+', 'A', 'B+', 'B', 'C', 'D'],
        datasets: [
          {
            label: 'Cardio Score by Cluster',
            backgroundColor: ['#48b6c8', '#b6c294', '#bcbf8a', '#51c1d2' ,'#42abba', '#84aad8'],
            data: [40, 20, 12, 20, 15, 23]
          }
        ]
      }
    }
  }
}
</script>