<template>
	<ul class="list">
		<li class="item"
		v-for="(item,key) of citys"
		:key="key"
		@click="handLetterClick"
		>{{key}}</li>
	</ul>
</template>
<script>
export default {
  name: 'CityAlphabet',
  props: {
    citys: Object
  },
  methods: {
    handLetterClick (e) {
      this.$emit('change', e.target.innerText)
    }
  }
}
</script>
<style lang="stylus" scoped>
@import '~styles/varibles.styl';
	.list
		position fixed
		top 25%
		right 0.5rem
		.item
			text-align center
			color $bgcolor
			margin-top .2rem
</style>
