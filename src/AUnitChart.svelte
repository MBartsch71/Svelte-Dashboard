<script>
  import { onMount } from 'svelte'
  import Chart from 'chart.js'

  function createChart() {
    var ctx = document.getElementById('AUnitChart')
    var myChart = new Chart(ctx, {
      type: 'doughnut',
      data: {
        datasets: [
          {
            label: '# of Votes',
            data: [65, 35],
            backgroundColor: ['#31d214', '#fa0505'],
            borderColor: ['#193549', '#193549'],
            borderWidth: 1,
          },
        ],
      },
      options: {
        circumference: Math.PI,
        rotation: -Math.PI,
        cutoutPercentage: 60,
      },
    })
  }

  onMount(createChart)
</script>

<style>
  .chart {
    border-radius: 4px;
    background: rgb(2, 0, 36);
    background: linear-gradient(0deg, #193549 0%, #15232d 100%);
    width: 48%;
    height: 48%;
    display: flexbox;
    float: left;
    margin: 0.5rem;
    box-sizing: border-box;
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

<div class="chart">
  <p class="p-header">Overall AUnit coverage</p>
  <div class="chart-content">
    <canvas id="AUnitChart" width="30%" height="20%" />
  </div>
</div>
