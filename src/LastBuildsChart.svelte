<script>
  import { onMount } from 'svelte'
  import Chart from 'chart.js'

  function createChart() {
    var ctx = document.getElementById('LBChart')
    var myChart = new Chart(ctx, {
      type: 'horizontalBar',
      data: {
        labels: [
          'ZCL_TC_ACT_HDL',
          'ZCL_TC_HELP',
          'ZCL_TC_CAMT054_DD',
          'ZCL_HZV_REFERENCE',
          'ZCL_A64_MP04_OUT',
          'ZCL_TC_REGEX',
          'ZCL_HZV_ESR_REFERENCE',
          'ZCL_TC_ACTION',
          'ZCL_TC_ACT_PAR_M',
          'ZCL_UNIT_TEST',
          'ZCL_11',
          'ZCL_12',
          'ZCL_13',
          'ZCL_14',
          'ZCL_15',
        ],
        datasets: [
          {
            fill: 'end',
            data: [88, 92, 58, 75, 80, 65, 72, 77, 86, 95, 83, 86, 77, 62, 92],
            backgroundColor: [
              'lime',
              'lime',
              'red',
              'orange',
              'lime',
              'red',
              'orange',
              'orange',
              'lime',
              'lime',
              'lime',
              'lime',
              'orange',
              'red',
              'lime',
            ],
            borderColor: 'orange',
            lineTension: 0,
          },
        ],
      },
      options: {
        legend: {
          display: false,
          position: 'top',
          labels: {
            boxWidth: 80,
            fontColor: 'white',
          },
          plugins: {
            filler: {
              propagate: true,
            },
          },
        },
        scales: {
          yAxes: [
            {
              ticks: {
                max: 100,
                min: 0,
                stepSize: 10,
                fontColor: 'orange',
              },
            },
          ],
          xAxes: [
            {
              ticks: {
                min: 0,
                max: 100,
                stepsize: 10,
                fontColor: 'orange',
              },
            },
          ],
        },
      },
    })
  }

  onMount(createChart)
</script>

<style>
  .LBChart {
    border-radius: 4px;
    background: rgb(2, 0, 36);
    background: linear-gradient(0deg, #193549 0%, #15232d 100%);
    width: 100%;
    height: 100%;
    margin: 0.5rem 0rem;
    box-sizing: border-box;
    float: none;
  }

  .chart-content {
    padding: 0;
  }

  .p-header {
    border-bottom: 1px solid white;
    padding: 0.2rem 1rem;
    margin: 0;
    text-align: left;
  }
</style>

<div class="LBChart">
  <p class="p-header">Last Builds Coverage</p>
  <div class="chart-content">
    <canvas id="LBChart" width="70%" height="100%" />
  </div>
</div>
