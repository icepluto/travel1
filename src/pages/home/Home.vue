<template>
<div>
  <home-header></home-header>
  <home-swiper></home-swiper>
</div>
</template>

<script>
import HomeHeader from './components/Header.vue'
import HomeSwiper from './components/Swiper.vue'
import HomeRecommend from './components/Recommend.vue'
export default {
  name: 'Home',
  components: {
    HomeHeader,
    HomeSwiper,
    HomeRecommend
  }
}
</script>

<style>
</style>
