<template>
  <div>
    <detail-banner></detail-banner>
    <detail-header></detail-header>
    <div class="content">
      <detail-list :lists="lists"></detail-list>
    </div>
  </div>
</template>

<script>
import DetailBanner from './components/Banner'
import DetailHeader from './components/header'
import DetailList from './components/List'
export default {
  name: 'Detail',
  components: {
    DetailBanner,
    DetailHeader,
    DetailList
  },
  data () {
    return {
      lists: [{
        title: '成人票',
        children: [{
          title: '成人票三人联票',
          children: [{
            title: '成人票三人联票-特价机票'
          }, {
            title: '成人票三人联票-特价酒店'
          }]
        }, {
          title: '成人票四人联票'
        }, {
          title: '成人票五人联票'
        }]
      }, {
        title: '学生票'
      }, {
        title: '儿童票'
      }, {
        title: '特价票'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  .content
    height: 50rem
</style>
