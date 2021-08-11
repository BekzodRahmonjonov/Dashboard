<template>
  <div class="appointment-activity">
    <header class="appointment-activity__header">
      <h3 class="heading">Appointment Activity</h3>
    </header>
    <AppointmentTable />
  </div>
</template>

<script>
import AppointmentTable from './AppointmentTable.vue'
export default {
  components: {
    AppointmentTable,
    
  }
}
</script>

<style lang="scss">
  .appointment-activity {
    background: #FFFFFF;
    box-shadow: 0px 12px 26px rgba(16, 30, 115, 0.06);
    border-radius: 8px;
    margin-top: 30px;
    &__header {
      padding: 24px 24px 18px;
    }
  }
  
</style>