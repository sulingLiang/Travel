<template>
  <div class="list" ref="wrapper">
    <div>
      <div class="area">
        <div class="title border-topbottom">当前位置</div>
        <div class="button-list">
          <div class="button-wrapper">
            <div class="item">北京</div>
          </div>
        </div>
      </div>
      <div class="area">
        <div class="title">热门城市</div>
        <div class="button-list" >
          <div class="button-wrapper" v-for="item in hotCities" :key="item.id">
            <div class="item">{{item.name}}</div>
          </div>
        </div>
      </div>
      <div class="area" v-for="(item, key) in cities" :key="key">
        <div class="title">{{key}}</div>
        <div class="item-list" v-for="innerItem in item" :key="innerItem.id">
          <div class="item border-bottom">{{innerItem.name}}</div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import BScroll from 'better-scroll'
export default {
  name: 'CityList',
  props: {
    cities: Object,
    hotCities: Array
  },
  mounted () {
    this.scroll = new BScroll(this.$refs.wrapper)
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/variable.styl'
  .list
    overflow: hidden
    position: absolute
    top: 1.58rem
    left: 0
    right: 0
    bottom: 0
    .title
      height: .32rem
      background: #eee
      padding: .2rem .1rem
    .button-list
      overflow: hidden
      padding: .1rem .6rem .1rem .1rem
      .button-wrapper
        float: left
        width: 33.33%
        .item
          margin: .1rem
          padding: .1rem
          border: .02rem solid #eee
          text-align: center
          border-radius: .06rem
    .item-list
      padding-left: .2rem
      .item
        height: .24rem
        line-height: .24rem
        padding: .2rem 0
</style>
