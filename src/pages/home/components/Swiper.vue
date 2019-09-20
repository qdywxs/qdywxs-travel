<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
      <swiper-slide v-for="item of swiperList" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl">
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
        pagination: '.swiper-pagination',
        loop: true,
        autoplay: 3000
      },
      swiperList: [{
        id: '0001',
        imgUrl: 'https://qdywxs.github.io/travel-images/swiperList01.jpg'
      }, {
        id: '0002',
        imgUrl: 'https://qdywxs.github.io/travel-images/swiperList02.jpg'
      }, {
        id: '0003',
        imgUrl: 'https://qdywxs.github.io/travel-images/swiperList03.jpg'
      }, {
        id: '0004',
        imgUrl: 'https://qdywxs.github.io/travel-images/swiperList04.jpg'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
.wrapper >>> .swiper-pagination-bullet-active
  background: #fff
.wrapper
  overflow: hidden
  width: 100%
  height: 0
  padding-bottom: 31.25%
  background: #eee
  .swiper-img
    width: 100%
</style>
