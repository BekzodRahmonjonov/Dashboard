<template>
  <div class="intro-card">
    <img :src="icon" alt="Intro Card Icon">
    <div class="intro-card__item">
      <h5 class="heading_sm"> {{ title }} </h5>
      <h4 class="heading"> {{ number }} </h4>
    </div>
  </div>
</template>

<script>
export default {
  props: ['title', 'icon', 'number']
}
</script>

<style lang="scss">
  .intro-card {
    background: #FFFFFF;
    box-shadow: 0px 12px 26px rgba(16, 30, 115, 0.06);
    border-radius: 8px;
    padding: 20px 24px;
    display: flex;
    align-items: center;
    gap: 24px;
    width: 255px;
    &__item {
      display: flex;
      flex-direction: column;
      gap: 4px;
      .heading_sm {
        color: #000;
      }
      .heading {
        color: #336CFB;
      }
    }
  }
</style>