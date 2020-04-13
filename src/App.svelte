<script>
  import AUnitChart from './AUnitChart.svelte'
  import TestToolChart from './TestToolChart.svelte'
  import AUnitHistory from './AUnitHistory.svelte'
  import LastBuildsChart from './LastBuildsChart.svelte'
</script>

<style>
  .header {
    display: flexbox;
    width: 100%;
    height: 10%;
    padding: 0 0.5rem;
  }
  .leftBox {
    float: left;
    height: 90%;
    width: 65%;
  }

  .rightBox {
    float: left;
    height: 90%;
    width: 34%;
  }
</style>

<div class="header">
  <h1>CQA Dashboard - DE2</h1>

</div>

<div class="leftBox">
  <AUnitChart />
  <TestToolChart />
  <AUnitHistory />
</div>

<div class="rightBox">
  <LastBuildsChart />
</div>
