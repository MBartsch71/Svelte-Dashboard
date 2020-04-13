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
    <ul>
      <li class="li">ZCL_TC_ACT_HDL</li>
      <li class="li">ZCL_TC_HELP</li>
      <li class="li">ZCL_TC_CAMT054_DD</li>
      <li class="li">ZCL_HZV_REFERENCE</li>
      <li class="li">ZCL_A64_MP04_OUT</li>
      <li class="li">ZCL_TC_REGEX</li>
      <li class="li">ZCL_HZV_ESR_REFERENCE</li>
      <li class="li">ZCL_TC_ACTION</li>
      <li class="li">ZCL_TC_ACT_PAR_M</li>
      <li class="li">ZCL_UNIT_TEST</li>
    </ul>
    <canvas id="LasstBuilds" width="100%" height="20%" />
  </div>
</div>
