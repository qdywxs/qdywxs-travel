<template>
  <div>
    <div class="title">用户评论</div>
    <div
      class="comment border-bottom"
      v-for="item of commentList"
      :key="item.id"
    >
      <div class="stardate">
         <p class="star-level">{{item.star}}</p>
         <p class="comment-date">{{item.date}}</p>
      </div>
      <p class="comment-content">{{item.content}}</p>
      <div class="imgs">
        <div
          class="img-wrapper"
          v-for="(innerItem, index) of item.imgUrl"
          :key="index"
        >
          <img :src="innerItem" class="comment-img">
        </div>
      </div>

    </div>
  </div>
</template>

<script>
export default {
  name: 'DetailComment',
  data () {
    return {
      commentList: [{
        id: '0001',
        star: '★★★★★',
        date: 'q*9  2019-11-01',
        content: '我们是早上8:30的第一场，有珍宝馆的套票，王蕾导游讲解很到位，妙语连珠，互动性强，服务热情，路线和讲解安排合理，游玩很开心有意义，对故宫有了深入全面的了解，不虚此行，不留遗憾，深有体会，故宫博物院完美打卡。',
        imgUrl: ['https://qdywxs.github.io/travel-images/commentImg01.jpg', 'https://qdywxs.github.io/travel-images/commentImg02.jpg', 'https://qdywxs.github.io/travel-images/commentImg03.jpg', 'https://qdywxs.github.io/travel-images/commentImg04.jpg', 'https://qdywxs.github.io/travel-images/commentImg05.jpg', 'https://qdywxs.github.io/travel-images/commentImg06.jpg']
      }, {
        id: '0002',
        star: '★★★★★',
        date: 'z*3  2019-11-01',
        content: '非常好的体验，推荐大福晋导游。故宫太大，又是历史文化浓重的宫殿，如果没有导游，自己瞎逛浪费时间和体力，也不明白很多殿的故事，每个人一个无线耳麦，离导游三十米内都听的很清楚，导游讲解的风趣幽默，不错的一次体验。',
        imgUrl: ['https://qdywxs.github.io/travel-images/commentImg01.jpg', 'https://qdywxs.github.io/travel-images/commentImg02.jpg', 'https://qdywxs.github.io/travel-images/commentImg03.jpg', 'https://qdywxs.github.io/travel-images/commentImg04.jpg', 'https://qdywxs.github.io/travel-images/commentImg05.jpg', 'https://qdywxs.github.io/travel-images/commentImg06.jpg']
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
.title
  margin-top: .2rem
  line-height: .8rem
  background: #eee
  text-indent: .2rem
.comment
  padding: .1rem .2rem .2rem .2rem
  .stardate
    position: relative
    height: .6rem
    line-height: .6rem
    .star-level
      position: absolute
      float: left
      top: .15rem
      left: 0
      line-height: .3rem
      color: #ffb436
    .comment-date
      position: absolute
      float: right
      top: .15rem
      right: 0
      line-height: .3rem
      font-size: .24rem
  .comment-content
    line-height: .44rem
  .imgs
    overflow: hidden
    width: 100%
    height: 0
    padding-bottom: 50%
    .img-wrapper
      overflow: hidden
      float: left
      width: 32.85%
      height: 0
      padding-bottom: 23%
      margin: .1rem 0 0 .1rem
      &:nth-child(1),
      &:nth-child(4)
        margin-left: -.1rem
      .comment-img
        width: 100%
</style>
