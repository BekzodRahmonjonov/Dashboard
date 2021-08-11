<template>
  <div class="intro">
    <IntroCard v-for="(item, index) in IntroCard" :key="index" :title="item.title" :number="item.number" :icon="item.icon" />
  </div>
</template>

<script>
import IntroCard from './IntroCard.vue'
export default {
  components: {
    IntroCard
  },
  data () {
    return {
      IntroCard: [
        {
          icon: require('../assets/intro-icon.svg'),
          title: 'Appointments',
          number: 213
        },
        {
          icon: require('../assets/intro-icon2.svg'),
          title: 'New Patients',
          number: 104
        },
        {
          icon: require('../assets/intro-icon3.svg'),
          title: 'Operations',
          number: 24
        },
        {
          icon: require('../assets/intro-icon4.svg'),
          title: 'Hospital Earnings',
          number: '$ 12,174'
        }
      ]
    }
  }
}
</script>

<style lang="scss">
  .intro {
    display: flex;
    justify-content: space-between;
    padding: 8px 0;
  }
</style>