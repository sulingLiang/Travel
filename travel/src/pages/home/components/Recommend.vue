<template>
  <div>
    <div class="title">热销组件</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
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
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1607/7c/7cda8b6782dabd80b4.img.jpg_200x200_2039e660.jpg',
        title: '上海迪士尼乐园',
        desc: '随买随用'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1811/e4/e4b9b471d2afc473a3.img.jpg_200x200_9a7794fc.jpg',
        title: '上海欢乐谷',
        desc: '随买随用'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/tuan/team2/1507/2c/83e0e0e7ae082a.jpg_200x200_6d7378b2.jpg',
        title: '东方明珠',
        desc: '随买随用随买随用随买随用随买随用随买随用随买随用'
      }]
    }
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
