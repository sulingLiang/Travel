<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
      <swiper-slide v-for="item of swiperList" :key="item.id">
        <img :src="item.imgUrl" alt="swiper" class="swiper-img">
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
        pagination: {
          el: '.swiper-pagination'
        },
        loop: true
      },
      swiperList: [
        {
          id: '001',
          imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20191/99d97f5421741c2a2028dced52b66391.jpg_750x200_9e38628d.jpg'
        }, {
          id: '002',
          imgUrl: 'http://img1.qunarzz.com/piao/fusion/1812/d1/cd4f32e924a5a302.jpg_750x200_3d492837.jpg'
        }
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
  .wrapper >>> .swiper-pagination-bullet-active
    background: #fff
  .wrapper
    width: 100%
    overflow: hidden
    height: 0
    padding-bottom: 26.68%
    .swiper-img
      width: 100%
</style>
