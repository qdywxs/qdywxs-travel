<template>
  <div>
    <router-link
      tag="div"
      to="/"
      class="header-abs"
      v-show="showAbs"
    >
      <span class="iconfont header-abs-back">&#xe658;</span>
    </router-link>
    <div
      class="header-fixed"
      v-show="!showAbs"
      :style="opacityStyle"
    >
      <router-link to="/">
        <span class="iconfont header-fixed-back">&#xe658;</span>
      </router-link>
      景点详情
    </div>
  </div>
</template>

<script>
export default {
  name: 'DetailHeader',
  data () {
    return {
      showAbs: true,
      opacityStyle: {
        opacity: 0
      }
    }
  },
  methods: {
    handleScroll () {
      const top = document.documentElement.scrollTop

      if (top > 50) {
        let opacity = top / 150
        opacity = opacity > 1 ? 1 : opacity

        this.opacityStyle = {opacity}
        this.showAbs = false
      } else {
        this.showAbs = true
      }
    }
  },
  mounted () {
    window.addEventListener('scroll', this.handleScroll)
  },
  beforeDestory () {
    window.removeEventListener('scroll', this.handleScroll)
  }
}
</script>

<style lang="stylus" scoped>
@import '~styles/varibles.styl'
.header-abs
  position: absolute
  top: .2rem
  left: .2rem
  width: .8rem
  height: .8rem
  line-height: .8rem
  text-align: center
  border-radius: .4rem
  background: rgba(0, 0, 0, .8)
  .header-abs-back
    color: #fff
    font-size: .56rem
.header-fixed
  position: fixed
  top: 0
  left: 0
  right: 0
  z-index: 2
  height: $headerHeight
  line-height: $headerHeight
  color: #fff
  text-align: center
  font-size: .32rem
  background: $bgColor
  .header-fixed-back
    position: absolute
    top: 0
    left: 0
    width: .64rem
    text-align: center
    font-size: .56rem
    color: #fff
</style>
