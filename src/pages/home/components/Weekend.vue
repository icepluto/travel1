<template>
<div>
  <div class="title">周末去哪儿</div>
  <ul>
    <li class="item border-bottom" v-for="item of list" :key="item.id" >
      <div class="item-img-wrapper">
					<img class="item-img" :src="item.imgUrl" alt="">
			</div>
      <div class="item-info">
        <p class="item-title">{{item.title}}</p>
        <p class="item-desc">{{item.desc}}</p>
      </div>
    </li>
  </ul>
</div>
</template>
<script>
export default {
  name: 'HomeWeekend',
  props: {
    list: Array
  }
}
</script>
<style lang="stylus" scoped>
  .title
    width 100%
    background-color #eee
    font-size 16px
    height 2rem
    line-height 2rem
    text-indent 1rem
  .item-img
    width 100%
  .item-info
    flex 1
    padding .5rem
    .item-title
      font-size 1.2rem
      padding .2rem
    .item-desc
      font-size .8rem
      padding .2rem
      line-height 1rem
      color #ccc
</style>
