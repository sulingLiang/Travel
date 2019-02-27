<template>
  <div>
    <div v-for="(item, index) in lists" :key="index" class="item">
      <div class="item-title border-bottom">
        <div class="item-title-icon"></div>
        <div class="item-title-info">{{item.title}}</div>
      </div>
      <div v-if="item.children" class="item-children">
        <detail-list :lists="item.children"></detail-list>
      </div>
    </div>
  </div>
</template>

<script>

export default {
  name: 'DetailList',
  props: {
    lists: Array
  }
}
</script>

<style lang="stylus" scoped>
  .item-title
    display: flex
    line-height: .8rem
    padding: 0 .2rem
    font-size: .32rem
    .item-title-icon
      display: inline-block
      position: relative
      left: .1rem
      top: .2rem
      padding-right: .1rem
      width: .36rem
      height: .36rem
      background: url(http://s.qunarzz.com/piao/image/touch/sight/detail.png) 0 -.45rem no-repeat
      margin-right: .1rem
      background-size: .4rem 3rem
    .item-title-info
      flex: 1
  .item-children
    padding: 0 .2rem
</style>
