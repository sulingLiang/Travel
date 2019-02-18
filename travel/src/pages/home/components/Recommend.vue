<template>
  <div>
    <div class="title">热销组件</div>
    <ul>
      <li class="item border-bottom" v-for="item of list" :key="item.id">
        <img class="item-img" :src="item.imgUrl" :alt="item.title">
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-button">查看详情</button>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  props: {
    list: Array
  }
}
</script>

<style lang="stylus" scoped>
  @import "~styles/mixins.styl"
  .title
    padding: .2rem
    text-indent: .2rem
    font-size: .32rem
    background: #e8e6e6
  .item
    overflow: hidden
    display: flex
    height: 1.9rem
    .item-img
      width: 1.7rem
      height: 1.7rem
      padding: .1rem
    .item-info
      flex: 1
      min-width: 0
      .item-title
        padding: .2rem .1rem
        font-size: .32rem
        ellipsis()
      .item-desc
        padding: 0 .1rem .1rem
        color: #ccc
        ellipsis()
      .item-button
        font-size: .24rem
        color: #fff
        margin: .1rem .1rem
        background: #ff8100
</style>
