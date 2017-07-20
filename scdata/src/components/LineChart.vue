<template>
  <div>
  </div>
</template>

    <script>
      import {Line, mixins} from 'vue-chartjs' // We specify what type of chart we want from vue-chartjs and the mixins module
      const { reactiveProp } = mixins
      export default Line.extend({ //We are extending the base chart class as mentioned above
        mixins: [reactiveProp],
        data () {
          return {
            options: {
              scales: {
                yAxes: [{
                  ticks: {
                    beginAtZero: true
                  },
                  gridLines: {
                    display: true
                  }
                }],
                xAxes: [ {
                  gridLines: {
                    display: false
                  }
                }]
              },
              legend: {
                display: true
              },
              responsive: true,
              maintainAspectRatio: false
            }
          }
        },
        mounted () {
          // this.chartData is created in the mixin
          this.renderChart(this.chartData, this.options)
        }
      })
    </script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
body{
	font-weight: normal;
}
h1{
  font-size:3em;
	font-weight: normal;
	margin-top:0;
}
p{
	font-size:0.9em;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #42b983;
}
</style>
