<template>
  <Pie :chart-data="chartData" :width="width" :height="height"/>
</template>

<script>
import { Pie } from 'vue-chartjs/legacy'
import {
  Chart as ChartJS,
  Title,
  Tooltip,
  Legend,
  ArcElement,
  CategoryScale,
} from 'chart.js'

ChartJS.register(Title, Tooltip, Legend, ArcElement, CategoryScale)


export default {
  name: 'PieChart',
  components: { Pie },
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
        labels: [ 'Female Weanling', 'Male Weanling', 'Female Yearling', 'Male Yearling', 'Female 2YO', 'Male 2YO', 'Female Older', 'Male Older'],
        datasets: [
          {
            // label: 'Population with Biomechanics',
            backgroundColor: ['#50bad5','#9094ee','#859fe9', '#78adfe', '#5aadd8', '#58b6ec', '#75b0ec', '#92c792'],
            data: [10, 5, 2, 10, 6, 9, 4, 15]
          }
        ]
      },
    }
  }
}
</script>