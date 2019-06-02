<template>
<div class="header">
  <div class="header-left">
    <span class="iconfont back-icon"></span>
  </div>
  <div class="header-input">
    <span class="iconfont"></span>
    输入城市/游玩/主题
  </div>
  <div class="header-right">
    城市
    <span class="iconfont"></span>
  </div>
</div>
</template>

<script>
export default {
  name: 'HomeHeader'
}
</script>

<style lang="stylus" scoped>
  .header
    display flex
    line-height 3rem
    background-color blue
    color #ffffff
    .header-left
      width 2rem
      line-height 3rem
      padding-left .5rem
      float left
      .back-icon
        font-size 2rem
    .header-input
      flex 1
      background #fff
      padding-left 0.4rem
      height 2rem
      line-height 1.8rem
      border-radius .5rem
      margin-top .6rem
      margin-left 0.4rem
      color #cccccc
    .header-right
      width 4.24rem
      height 3rem
      float right
      text-align center
</style>
