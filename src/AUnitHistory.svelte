<script>
  import { onMount } from 'svelte'
  import Chart from 'chart.js'

  function createChart() {
    var ctx = document.getElementById('AUHChart')
    var myChart = new Chart(ctx, {
      type: 'line',
      data: {
        labels: [
          '1',
          '2',
          '3',
          '4',
          '5',
          '6',
          '7',
          '8',
          '9',
          '10',
          '11',
          '12',
          '13',
          '14',
          '15',
          '16',
          '17',
          '18',
          '19',
          '20',
          '21',
          '22',
          '23',
          '24',
          '25',
          '26',
          '27',
          '28',
          '29',
          '30',
        ],
        datasets: [
          {
            fill: 'start',
            data: [
              80,
              60,
              58,
              75,
              80,
              65,
              72,
              77,
              86,
              74,
              71,
              77,
              82,
              69,
              76,
              85,
              83,
              85,
              69,
              65,
              76,
              77,
              60,
              55,
              76,
              87,
              91,
              82,
              91,
              92,
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
  .AUHchart {
    border-radius: 4px;
    background: rgb(2, 0, 36);
    background: linear-gradient(0deg, #193549 0%, #15232d 100%);
    width: 97%;
    height: 20%;
    display: flexbox;
    margin: 0.5rem;
    box-sizing: border-box;
    float: left;
  }

  .chart-content {
    padding: 0.5rem;
  }

  .p-header {
    border-bottom: 1px solid white;
    padding: 0.2rem 1rem;
    margin: 0;
    text-align: left;
  }
</style>

<div class="AUHchart">
  <p class="p-header">AUnit History - Last 30 days</p>
  <div class="chart-content">
    <canvas id="AUHChart" width="100%" height="30%" />
  </div>
</div>
