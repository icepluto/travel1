<template>
<div>
	<router-link to="/" tag="div" class="header-back" v-show="showAbs">
    <div class="iconfont header-icon">&#xe658;</div>
	</router-link>
  <div class="header-fixed" v-show="!showAbs" :style="opacityStyle">
    <router-link to='/' tag="div">
			<div class="header-fixed-left iconfont">&#xe658;</div>
		</router-link>
		详情选择
	</div>
</div>
</template>
<script>
export default {
  name: 'DetailHeader',
  data () {
    return {
      showAbs: true,
      opacityStyle: {
        opacity: 0
      }
    }
  },
  methods: {
    handleScroll () {
      const top = document.documentElement.scrollTop
      if (top > 60) {
        let opacity = top / 140
        opacity = opacity > 1 ? 1 : opacity
        this.opacityStyle = { opacity }
        this.showAbs = false
      } else {
        this.showAbs = true
      }
    }
  },
  activated () {
    window.addEventListener('scroll', this.handleScroll)
  },
  deactivated () {
    window.removeEventListener('scroll', this.handleScroll)
  }
}
</script>
<style lang="stylus" scoped>
@import '~styles/varibles.styl';
  .header-back
    position absolute
    width 2rem
    height 2rem
    border-radius 50%
    background-color black
    text-align center
    line-height 2rem
    opacity 0.5
    top 0
    left 0
    margin .5rem
    .header-icon
      color #ffffff
      font-size 2rem
  .header-fixed
    position fixed
    top 0
    left 0
    z-index 2
    background-color $bgcolor
    width 100%
    height 2rem
    line-height 2rem
    text-align center
    color #fff
		.header-fixed-left
			width 3rem
			position absolute
			top 0
			color #fff
      font-size 10rem
</style>
