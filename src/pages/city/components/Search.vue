<template>
  <div>
    <div class="search">
      <input class="search-input" v-model="keyword" type="text" placeholder="输入城市名或拼音">
    </div>
    <div class="search-content" ref="search"
      v-show="keyword"
    >
      <ul>
        <li class="search-item border-bottom" v-for="item of list" :key="item.id">
          {{item.name}}
        </li>
        <li class="search-item border-bottom search-bg-item" v-show="!list.length">
          没有匹配数据
        </li>
      </ul>
    </div>
  </div>
</template>
<script>
export default {
  name: 'CitySearch',
  props: {
    citys: Object
  },
  data () {
    return {
      keyword: '',
      list: [],
      timer: null
    }
  },
  watch: {
    keyword () {
      if (this.timer) {
        clearTimeout(this.timer)
      }
      if (!this.keyword) {
        this.list = []
        return
      }
      this.timer = setTimeout(() => {
        const result = []
        for (let i in this.citys) {
          this.citys[i].forEach((value) => {
            if (value.pinyin.indexOf(this.keyword) > -1 ||
            value.name.indexOf(this.keyword) > -1) {
              result.push(value)
            }
          })
        }
        this.list = result
      }, 100)
    }
  },
  mounted () {
    this.scroll = new Bscroll(this.$refs.search)
  }
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
.search-content
  z-index 1
  position absolute
  top 4.5rem
  left 0
  right 0
  bottom 0
  background-color #eee
  .search-item
    line-height 1rem
    background-color #ffffff
    color #666
  .search-bg-item
    background-color #eee
</style>
