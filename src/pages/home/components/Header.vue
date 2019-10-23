<template>
  <div class="header">
    <div class="header-left">
      <span class="iconfont back-icon">&#xe658;</span>
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe63c;</span>
      输入城市/景点/游玩主题
    </div>
    <router-link to="/city">
      <div class="header-right">
        {{this.city}}
        <span class="iconfont arrow-icon">&#xe65c;</span>
      </div>
    </router-link>
  </div>
</template>

<script>
import { mapState } from 'vuex'
export default {
  name: 'HomeHeader',
  computed: {
    ...mapState(['city'])
  }
}
</script>

<style lang="stylus" scoped>
@import '~styles/varibles.styl'
.header
  display: flex
  line-height: $headerHeight
  color: #fff
  background: $bgColor
  .header-left
    float: left
    width: .64rem
    .back-icon
      display: block
      text-align: center
      font-size: .56rem
  .header-input
    flex: 1
    margin-top: .12rem
    margin-left: .2rem
    padding-left: .12rem
    height: .64rem
    line-height: .64rem
    color: #ccc
    background: #fff
    border-radius: .1rem
  .header-right
    float: right
    min-width: 1.04rem
    padding: 0 .1rem
    text-align: center
    color: #fff
    .arrow-icon
      margin-left: -0.1rem
</style>
