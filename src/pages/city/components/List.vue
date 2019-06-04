<template>
	<div class="list">
		<div class="area">
			<div class="title border-topbottom">当前城市</div>
			<div class="button-list">
				<div class="button-wrapper">
					<div class="button">北京</div>
				</div>
				<div class="button-wrapper">
					<div class="button">北京</div>
				</div>
				<div class="button-wrapper">
					<div class="button">北京</div>
				</div>
				<div class="button-wrapper">
					<div class="button">北京</div>
				</div>
				<div class="button-wrapper">
					<div class="button">北京</div>
				</div>
			</div>
		</div>
		<div class="area">
			<div class="title border-topbottom">热门城市</div>
			<div class="button-list">
				<div class="button-wrapper">
					<div class="button">北京</div>
				</div>
				<div class="button-wrapper">
					<div class="button">北京</div>
				</div>
				<div class="button-wrapper">
					<div class="button">北京</div>
				</div>
				<div class="button-wrapper">
					<div class="button">北京</div>
				</div>
				<div class="button-wrapper">
					<div class="button">北京</div>
				</div>
			</div>
		</div>
		<div class="area">
			<div class="title border-topbottom">A</div>
			<div class="item-list">
				<div class="item">阿拉尔</div>
				<div class="item">阿拉尔</div>
				<div class="item">阿拉尔</div>
				<div class="item">阿拉尔</div>
				<div class="item">阿拉尔</div>
				<div class="item">阿拉尔</div>
				<div class="item">阿拉尔</div>
				<div class="item">阿拉尔</div>
				<div class="item">阿拉尔</div>
				<div class="item">阿拉尔</div>
				<div class="item">阿拉尔</div>
				<div class="item">阿拉尔</div>
			</div>
		</div>
	</div>
</template>
<script>
export default {
  name: 'CityList'
}
</script>
<style lang="stylus" scoped>
	.border-topbottom
		&:before
			border-color #777777
		&:after
			border-color #777777
	.list
		overflow hidden
		position absolute
		top 4.5rem
		left 0
		right 0
		bottom 0
		.title
			line-height 2rem
			background-color #eee
			padding-left .5rem
			color #666666
		.button-list
			overflow hidden
			padding .2rem 2.2rem .2rem .2rem
			.button-wrapper
				width 33.33%
				float left
				.button
					margin .3rem
					text-align center
					border .08rem solid #8f9b9c
					border-radius .2rem
					padding .2rem 0
		.item-list
			.item
				margin .3rem .2rem
				border-bottom .08rem solid #eee
				padding .2rem 0
</style>
