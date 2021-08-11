<template>
  <div class="chart">
    <h3 class="heading">Hospital Survey</h3>
    <chart />
  </div>
</template>

<script>
import Chart from './Chart.vue'
export default {
  components: {
    Chart
    
  }
}
</script>

<style lang="scss">
  .chart {
    padding: 24px;
    background-color: #fff;
    border-radius: 8px;
    margin-top: 30px;
  }
</style>