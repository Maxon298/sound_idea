<template>
  <div class="selection">
    <h3 class="selection__title">{{title}}</h3>
    <div class="selection__dropdown">
      <div class="selection__dropdown_title">{{subtitle}}</div>
      <img src="@/assets/img/svg/dropdown__arrow.svg" alt="" class="selection__dropdown_arrow">
    </div>
  </div>
</template>

<script>
export default {
  name: "Selection",
  props: [
    'title',
    'subtitle',
  ]
}
</script>

<style lang="scss" scoped>
  .selection{
    position: relative;
    margin-top: 13px;
    width: 315px;
    height: 35px;
    border: 1px solid rgba(0, 0, 0, 0.3);
    &__title{
      position: absolute;
      top: -10px;
      left: 9px;

      border: 2px white solid;

      font-weight: 700;
      font-size: 10px;
      line-height: 12px;
      background-color: white;

      color: rgba(0, 0, 0, 0.3);
    }
    &__dropdown{
      margin: 10px 3px;

      display: flex;
      justify-content: space-between;

      font-weight: 700;
      font-size: 10px;
      line-height: 12px;

      color: #000000;
    }
  }
</style>





