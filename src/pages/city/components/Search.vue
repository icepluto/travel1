<template>
	<div class="search">
		<input class="search-input" type="text" placeholder="输入城市名或拼音">
	</div>
</template>
<script>
export default {
  name: 'CitySearch'
}
</script>
<style lang="stylus" scoped>
@import '~styles/varibles.styl';
	.search
		background $bgcolor
		text-align center
		.search-input
			box-sizing border-box
			padding 0 .5rem
			color #666666
			height 1.5rem
			text-align center
			width 88%
			margin .5rem
			border-radius .3rem
</style>
