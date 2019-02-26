<template>
  <div>
    <div class="banner" @click="handleBannerClick">
      <img class="banner-img" src="http://img1.qunarzz.com/wugc/p189/201206/12/a3ace34bc010041193835fbb.jpg_600x330_944cd8e9.jpg" alt="">
      <div class="banner-info">
        <div class="banner-title">南山文化旅游区(AAAAA景区)</div>
        <div class="banner-number">
          <span class="iconfont banner-icon">&#xe62e;</span>
          25
        </div>
      </div>
    </div>
    <common-gallary v-show="swiperStatus" @close="handleGallaryClose"></common-gallary>
  </div>
</template>

<script>
import CommonGallary from 'common/Gallary'
export default {
  name: 'DetailBanner',
  components: {
    CommonGallary
  },
  data () {
    return {
      swiperStatus: false
    }
  },
  methods: {
    handleBannerClick () {
      this.swiperStatus = true
    },
    handleGallaryClose () {
      this.swiperStatus = false
    }
  }
}
</script>

<style lang="stylus" scoped>
  .banner
    position: relative
    overflow: hidden
    height: 0
    padding-bottom: 55%
    .banner-img
      width: 100%
    .banner-info
      display: flex
      position: absolute
      left: 0
      right: 0
      bottom: 0
      line-height: .62rem
      background-image: linear-gradient(top, rgba(0, 0, 0, 0), rgba(0, 0, 0, 0.8))
      .banner-title
        flex: 1
        padding: 0 .2rem
        color: #fff
      .banner-number
        margin-top: .1rem
        color: #fff
        width: 1.24rem
        background: rgba(0,0,0,.5)
        height: .4rem
        line-height: .4rem
        border-radius: .3rem
        text-align: center
        font-size: .24rem
        margin-right: .2rem
        .banner-icon
          font-size: .24rem
</style>
