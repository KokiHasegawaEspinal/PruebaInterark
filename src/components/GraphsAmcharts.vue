<template>
    <div id="chartdiv">
        <Bar :data="chartData" :options="chartOptions" />  
        <Line :data="chartData" :options="chartOptions" /> 
        <Pie :data="chartData" :options="chartOptions" /> 
    </div>
</template>
    
  

<script>
import { Bar, Line, Pie } from 'vue-chartjs'
import { Chart as ChartJS, Title, Tooltip, Legend, BarElement, LineElement, PointElement, CategoryScale, LinearScale } from 'chart.js/auto'

ChartJS.register(Title, Tooltip, Legend, BarElement, LineElement, PointElement, CategoryScale, LinearScale)

export default {
  name: 'GraphsAmcharts',
  components: {
    Bar,
    Line,
    Pie
  },
  data() {
    return {
      chartData: {
        labels: ['January', 'February', 'March'],
        datasets: [
          {
            label: 'Data One',
            backgroundColor: '#f87979',
            data: [40, 20, 12]
          }
        ]
      },
      chartOptions: {
        responsive: true,
        maintainAspectRatio: false
      }
    }
  },
  mounted() {
    this.renderChart(this.chartData, this.chartOptions)
  }
}
</script>
  


<style scoped> 
 #chartdiv {
    width: 50%;
    height: 200px;
    
  }
</style>

