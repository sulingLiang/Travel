<template>
  <div>
    <div class="title">周末去哪儿</div>
    <ul>
      <li class="item border-bottom" v-for="item of list" :key="item.id">
        <div class="item-img-wrapper">
          <img class="item-img" :src="item.imgUrl" :alt="item.title">
        </div>
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeWeekend',
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
  .item-img-wrapper
    overflow: hidden
    height: 0
    padding-bottom: 33.4375%
    .item-img
      width: 100%
  .item-title
    padding: .2rem .1rem
    font-size: .32rem
    ellipsis()
  .item-desc
    padding: 0 .1rem .1rem
    color: #ccc
    ellipsis()
</style>
