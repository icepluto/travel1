<template>
<div>
	<detail-banner></detail-banner>
  <detail-header></detail-header>
  <div>
    <detail-list :list = 'list'></detail-list>
  </div>
</div>
</template>
<script>
import DetailBanner from './components/Banner'
import DetailHeader from './components/Header'
import DetailList from './components/List'
export default {
  name: 'Detail',
  components: {
    DetailBanner,
    DetailHeader,
    DetailList
  },
  data () {
    return {
      list: [{
        title: '学生票',
        children: [{
          title: '学生三馆联票',
          children: [{
            title: '学生三馆联票--欢乐谷'
          }, {
            title: '学生三馆联票--海上城'
          }]
        }, {
          title: '学生四馆联票'
        }]
      }, {
        title: '成人票'
      }, {
        title: '特价票'
      }, {
        title: '儿童票'
      }, {
        title: '打折票'
      }, {
        title: '打折票'
      }, {
        title: '打折票'
      }, {
        title: '打折票'
      }, {
        title: '打折票'
      }, {
        title: '打折票'
      }, {
        title: '打折票'
      }, {
        title: '打折票'
      }, {
        title: '打折票'
      }, {
        title: '打折票'
      }, {
        title: '打折票'
      }, {
        title: '打折票'
      }, {
        title: '打折票'
      }, {
        title: '打折票'
      }, {
        title: '打折票'
      }, {
        title: '打折票'
      }, {
        title: '打折票'
      }, {
        title: '打折票'
      }, {
        title: '打折票'
      }]
    }
  }
}
</script>
<style lang="stylus" scoped>
</style>
