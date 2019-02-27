<template>
  <div>
    <router-link tag="div" to="/" class="header-abs" v-show="showAbs">
      <div class="iconfont header-abs-icon">&#xe624;</div>
    </router-link>
    <div class="header-fixed" v-show="!showAbs" :style="opacityStyles">
      景点详情
      <router-link to="/">
        <div class="iconfont header-fixed-icon">&#xe624;</div>
      </router-link>
    </div>
  </div>
</template>

<script>

export default {
  name: 'DetailHeader',
  data () {
    return {
      showAbs: true,
      opacityStyles: {
        opacity: 0
      }
    }
  },
  methods: {
    handleScroll () {
      const top = document.documentElement.scrollTop
      if (top > 60) {
        let opacity = top / 140
        opacity = opacity > 1 ? 1 : opacity
        this.opacityStyles = { opacity }
        this.showAbs = false
      } else {
        this.showAbs = true
      }
    }
  },
  activated () {
    window.addEventListener('scroll', this.handleScroll)
  },
  deactivated () {
    window.removeEventListener('scroll', this.handleScroll)
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/variable.styl'
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
    .header-abs-icon
      color: #fff
      font-size: .32rem
  .header-fixed
    position: fixed
    z-index: 2
    top: 0
    left: 0
    width: 100%
    height: $headeHeight
    line-height: $headeHeight
    text-align: center
    color: #fff
    font-size: .32rem
    background: $bgColor
    .header-fixed-icon
      position: absolute
      top: 0
      left: 0
      width: .7rem
      height: .77rem
      text-align: center
      font-size: .36rem
      color: #fff
</style>
