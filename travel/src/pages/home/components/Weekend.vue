<template>
  <div>
    <div class="title">周末去哪儿</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
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
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1511/ea/7f43191b747bb9.jpg_r_640x214_f58e829d.jpg',
        title: '上海泡汤圣地',
        desc: '上海的朋友总会问，哪里可以泡温泉，哪里的温泉好呢？这里有最好最全的上海温泉'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1505/7d/df6ff468331c43.jpg_r_640x214_1f3783d0.jpg',
        title: '上海必打卡',
        desc: '中西合璧，现代和传统各有各的精彩'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/source/1603/ad/69b0fc5f48ad5f.jpg_r_640x214_b0fd5c7b.jpg',
        title: '周末亲子爱玩',
        desc: '走进自然或玩转乐园，感知大千世界，游乐项目惊险刺激，特色表演异彩纷呈，等你们~'
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
