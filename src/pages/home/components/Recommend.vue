<template>
<div>
  <div class="title">热销推荐</div>
  <ul>
    <li class="item border-bottom" v-for="item of recommendList" :key="item.id" >
      <img class="item-img" :src="item.imgUrl" alt="">
      <div class="item-info">
        <p class="item-title">{{item.title}}</p>
        <p class="item-desc">{{item.desc}}</p>
        <button class="item-button">查看详情</button>
      </div>
    </li>
  </ul>
</div>
</template>
<script>
export default {
  name: 'HomeRecommend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'static/timg(1).jpg',
        title: '西安海洋世界',
        desc: '浪漫快乐的天堂，是您的最佳选项，西安海洋世界欢迎您'
      }, {
        id: '0002',
        imgUrl: 'static/timg(2).jpg',
        title: '西安海洋世界',
        desc: '浪漫快乐的天堂，是您的最佳选项，西安海洋世界欢迎您'
      }, {
        id: '0003',
        imgUrl: 'static/timg(3).jpg',
        title: '西安海洋世界',
        desc: '浪漫快乐的天堂，是您的最佳选项，西安海洋世界欢迎您'
      }, {
        id: '0004',
        imgUrl: 'static/timg(4).jpg',
        title: '西安海洋世界',
        desc: '浪漫快乐的天堂，是您的最佳选项，西安海洋世界欢迎您'
      }]
    }
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
