<template>
  <div class="container">
    <Header />
    <Intro />
    <main-chart />
    <appointment-activity />
  </div>
</template>

<script>
import AppointmentActivity from './AppointmentActivity.vue'
import Header from './Header.vue'
import Intro from './Intro.vue'
import MainChart from './MainChart.vue'

export default {
  components: {
    Header,
    Intro,
    AppointmentActivity,
    MainChart,
  },
}
</script>

<style lang="scss">
  .container {
    margin-left: 256px;
    padding: 0 36px;
    background: #E5E5E5;
    width: 100px;
    height: 100vw;
    flex-basis: 84%;
    .add-modal {
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
    }
  }
</style>