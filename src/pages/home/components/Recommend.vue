<template>
<div>
  <div class="title">热销推荐</div>
  <ul>
    <router-link tag="li" :to="'/detail/' + item.id" class="item border-bottom" v-for="item of list" :key="item.id" >
      <img class="item-img" :src="item.imgUrl" alt="">
      <div class="item-info">
        <p class="item-title">{{item.title}}</p>
        <p class="item-desc">{{item.desc}}</p>
        <button class="item-button">查看详情</button>
      </div>
    </router-link>
  </ul>
</div>
</template>
<script>
export default {
  name: 'HomeRecommend',
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
  .item
    overflow hidden
    display flex
    height 6rem
    padding .1rem
    .item-img
      width 6rem
      height 6rem
    .item-info
      flex 1
      padding .5rem
      font-weight 600
      .item-title
        font-size 1.2rem
        padding .2rem
      .item-desc
        font-size .8rem
        padding .2rem
        line-height 1rem
        color #ccc
      .item-button
        background-color #ff9300
        border-radius 0.05rem
        color #fff
</style>
