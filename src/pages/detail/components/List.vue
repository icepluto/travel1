<template>
  <div>
    <div class="item" v-for="(item, index) of list" :key="index">
      <div class="item-title border-bottom">
        <span class="item-title-icon">
          {{item.title}}
        </span>
      </div>
      <div class="item-children" v-if="item.children">
        <detail-list :list = 'item.children'></detail-list>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: 'DetailList',
  props: {
    list: Array
  }
}
</script>
<style lang="stylus" scoped>
  .item-title
    font-size 1rem
    padding .2rem
    line-height 1.5rem
    background url('/static/icon.png') no-repeat
    background-size 1.5rem
    background-position 1% 50%
    .item-title-icon
      position relative
      left 1.5rem
      top .1rem
      line-height 1.5rem
  .item-children
    padding 0 .5rem
</style>
