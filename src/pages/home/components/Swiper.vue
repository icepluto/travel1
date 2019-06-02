<template>
<div class="wrapper">
  <swiper :options="swiperOption">
    <swiper-slide v-for="item of swiperList" :key="item.id">
      <img class="swiper-img" :src="item.imgUrl" alt="horse">
    </swiper-slide>
    <div class="swiper-pagination"  slot="pagination"></div>
  </swiper>
</div>
</template>
<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: {
          el: '.swiper-pagination'
        },
        loop: true
      },
      swiperList: [{
        id: '0001',
        imgUrl: 'http://pic37.nipic.com/20140113/8800276_184927469000_2.png'
      }, {
        id: '0002',
        imgUrl: 'http://pic37.nipic.com/20140113/8800276_184927469000_2.png'
      }]
    }
  }
}
</script>
<style lang="stylus" scoped>
  .wrapper
    overflow hidden
    width 100%
    height 0
    padding-bottom 50%
    background-color #eee
    .swiper-img
      width 100%
</style>
