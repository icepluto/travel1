<template>
	<div class="header">
		城市选择
		<router-link to='/'>
			<div class="header-left">
				<span class="iconfont back-icon">&#xe658;</span>
			</div>
		</router-link>
	</div>
</template>
<script>
export default {
  name: 'CityHeader'
}
</script>
<style lang="stylus" scoped>
@import '~styles/varibles.styl';
	.header
		position relative
		background-color $bgcolor
		color #fff
		height 2rem
		line-height 2rem
		text-align center
		.header-left
			width 3rem
			position absolute
			top 0
			color #fff
</style>
