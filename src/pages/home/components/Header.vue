<template>
<div class="header">
  <div class="header-left">
    <span class="iconfont back-icon">&#xe658;</span>
  </div>
  <div class="header-input">
    <span class="iconfont">&#xe611;</span>
    输入城市/游玩/主题
  </div>
  <router-link to='/city'>
    <div class="header-right">
      {{this.$store.state.city}}
      <span class="iconfont">&#xe612;</span>
    </div>
  </router-link>
</div>
</template>

<script>
import { mapState } from 'vuex'
export default {
  name: 'HomeHeader',
  computed: {
    ...mapState(['city'])
  }
}
</script>

<style lang="stylus" scoped>
@import '~styles/varibles.styl';
  .header
    display flex
    line-height 3rem
    background-color $bgcolor
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
      min-width 4.24rem
      height 3rem
      float right
      text-align center
      color #fff
</style>
