<template>
  <div class="container" @click ="handleGalleryClick">
    <div class="wrapper">
      <swiper class="content" :options="swiperOptions">
        <swiper-slide v-for="(item,index) in imgs" :key="index">
          <img class="gallery-img" :src="item" alt="horse">
        </swiper-slide>
        <div class="swiper-pagination"  slot="pagination"></div>
      </swiper>
    </div>
  </div>
</template>
<script>
export default {
  name: 'CommonGallery',
  props: {
    imgs: {
      type: Array,
      default () {
        return []
      }
    }
  },
  data () {
    return {
      swiperOptions: {
        pagination: '.swiper-pagination',
        paginationType: 'fraction',
        observer: true,
        observeParents: true
      }
    }
  },
  methods: {
    handleGalleryClick () {
      this.$emit('close')
    }
  }
}
</script>
<style lang="stylus" scoped>
  .container >>> .swiper-container
    overflow inherit
  .container
    display flex
    flex-direction column
    justify-content center
    z-index 10
    position fixed
    top 0
    right 0
    left 0
    bottom 0
    background-color #000
    .wrapper
      // overflow hidden
      width 100%
      height 0
      padding-bottom 70%
      color #fff
      .gallery-img
        width 100%
      .swiper-pagination
        color #ffffff
        bottom -2rem
        z-index 100
</style>
