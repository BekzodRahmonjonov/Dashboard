<template>
  <div class="aside-list">
    <span class="aside-list__icon" v-html="icon"></span>
    <h5 class="heading_sm"> {{ title }} </h5>
  </div>
</template>

<script>
export default {
  props: [
    'title',
    'icon'
  ]
}
</script>

<style lang="scss">
  .aside-list {
    display: flex;
    align-items: center;
    gap: 12px;
    padding: 14px 2px;
    cursor: pointer;
    &:hover {
      .heading_sm {
          color: #336CFB;
        }
      .aside-list__icon {
        path {
          fill: #336CFB;
        }
      }
    } 
  }
</style>