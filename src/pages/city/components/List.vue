<template>
	<div class="list" ref="wrapper">
		<div>
			<div class="area">
				<div class="title border-topbottom">当前城市</div>
				<div class="button-list">
					<div class="button-wrapper">
						<div class="button">{{this.$store.state.city}}</div>
					</div>
				</div>
			</div>
			<div class="area">
				<div class="title border-topbottom">热门城市</div>
				<div class="button-list">
					<div class="button-wrapper"
					v-for="item of hot"
					:key="item.id"
					@click="handCityClick(item.name)"
					>
						<div class="button">{{item.name}}</div>
					</div>
				</div>
			</div>
			<div class="area" v-for="(item,key) of citys" :key = "key" :ref="key">
				<div class="title border-topbottom">{{key}}</div>
				<div class="item-list">
					<div class="item" v-for="innerItem of item" :key="innerItem.id" @click="handCityClick(innerItem.name)">{{innerItem.name}}</div>
				</div>
			</div>
		</div>
	</div>
</template>
<script>
import Bscroll from 'better-scroll'
export default {
  name: 'CityList',
  props: {
    citys: Object,
    hot: Array,
    letter: String
  },
  methods: {
    handCityClick (city) {
      this.$store.commit('changeCity', city)
      this.$router.push('/')
    }
  },
  mounted () {
    this.scroll = new Bscroll(this.$refs.wrapper)
  },
  watch: {
    letter () {
      if (this.letter) {
        const element = this.$refs[this.letter][0]
        this.scroll.scrollToElement(element)
      }
    }
  }
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
