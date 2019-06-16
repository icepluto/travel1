<template>
	<div class="banner">
		<img class="banner-img" src="/static/banner/ban-1.jpg" alt="horse">
		<div class="banner-info">
			<div class="banner-title">welcome xi'an museum</div>
			<div class="banner-number">
				<span class="iconfont">&#xe658;</span>
				39
			</div>
		</div>
	</div>
</template>
<script>
export default {
  name: 'DetailBanner'
}

</script>
<style lang="stylus" scoped>
.banner
	position relative
	overflow hidden
	height 0
	padding-bottom 55%
	color #ffffff
	.banner-img
		width 100%
	.banner-info
		display flex
		position absolute
		left 0
		right 0
		bottom 0.5rem
		line-height 1.5rem
		.banner-title
			flex 1
			padding-left 0.5rem
		.banner-number
			padding-right 1rem
			background-color rgba(0,0,0,0.7)
			line-height 1.5rem
			border-radius 0.5rem 0 0 0.5rem
</style>
