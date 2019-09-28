<template>
  <div class="header">
    <router-link to="/">
      <span class="iconfont header-back">&#xe658;</span>
    </router-link>
    城市选择
  </div>
</template>

<script>
export default {
  name: 'CityHeader'
}
</script>

<style lang="stylus" scoped>
@import '~styles/varibles.styl'
.header
  position: relative
  overflow: hidden
  height: $headerHeight
  line-height: $headerHeight
  color: #fff
  text-align: center
  font-size: .32rem
  background: $bgColor
  .header-back
    position: absolute
    top: 0
    left: 0
    width: .64rem
    text-align: center
    font-size: .56rem
    color: #fff
</style>
