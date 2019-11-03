<template>
  <div>
    <detail-banner></detail-banner>
    <detail-header></detail-header>
    <detail-list :list="list"></detail-list>
    <detail-comment></detail-comment>
  </div>
</template>

<script>
import DetailBanner from './components/Banner'
import DetailHeader from './components/Header'
import DetailList from './components/List'
import DetailComment from './components/Comment'
export default {
  name: 'Detail',
  components: {
    DetailBanner,
    DetailHeader,
    DetailList,
    DetailComment
  },
  data () {
    return {
      list: [{
        title: '故宫当日票',
        children: [{
          title: '成人票',
          children: [{
            title: '故宫成人票+钟表馆+珍宝馆'
          }]
        }, {
          title: '学生票'
        }]

      }, {
        title: '故宫预售成人票'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
</style>
