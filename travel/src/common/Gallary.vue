<template>
  <div class="container" @click="handleGalleryClick">
    <div class="wrapper">
      <swiper :options="swiperOption">
        <swiper-slide>
          <img src="http://img1.qunarzz.com/sight/p0/1409/25/a173a55bb980f780d611b0e49dbf9890.jpg_r_800x800_9a34980b.jpg" alt="swiper" class="gallary-img">
        </swiper-slide>
        <swiper-slide>
          <img src="http://img1.qunarzz.com/sight/p0/1409/25/5a092cead73914a39f70c2140decfeb9.jpg_r_800x800_6486bfd6.jpg" alt="swiper" class="gallary-img">
        </swiper-slide>
        <div class="swiper-pagination" slot="pagination"></div>
      </swiper>
    </div>
  </div>
</template>

<script>
export default {
  name: 'CommonGallary',
  props: {
    imgs: {
      type: Array,
      default () {
        return []
      }
    }
  },
  data () {
    return {
      swiperOption: {
        pagination: {
          el: '.swiper-pagination',
          type: 'fraction'
        },
        observeParents: true,
        observer: true
      }
    }
  },
  methods: {
    handleGalleryClick () {
      this.$emit('close')
    }
  }
}
</script>

<style lang="stylus" scoped>
.container >>> .swiper-container
  overflow: inherit
.container
  display: flex
  flex-direction: column
  justify-content: center
  z-index: 99
  position: fixed
  left: 0
  right: 0
  top: 0
  bottom: 0
  background: #000
  .wrapper
    height: 0
    width: 100%
    padding-bottom: 100%
    .gallary-img
      width: 100%
      padding: 1.3rem 0
    .swiper-pagination
      color: #fff
      bottom: -1rem
</style>
