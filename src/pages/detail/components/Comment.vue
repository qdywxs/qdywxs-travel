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
  props: {
    commentList: Array
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
