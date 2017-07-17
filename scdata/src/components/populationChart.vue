<template>
  <div>
    <bar-cart></bar-cart>
  </div>
</template>

<script>
import { Bar } from 'vue-chartjs'

export default Bar.extend({
  data () {
    return {
      datacollection: {
        labels: ['1990', '2000', '2010' ],
        datasets: [
          {
            label: 'Data One',
            backgroundColor: '#f87979',
            data: ['24000', '221111', '222']
          }
        ]
      }
    }
  },
  mounted () {
    this.renderChart(this.datacollection, {responsive: true, maintainAspectRatio: false})
  }
})
</script>
<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
</style>
