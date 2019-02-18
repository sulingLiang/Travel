<template>
  <div class="header">
    <div class="header-left">
      <div class="iconfont back-icon">&#xe624;</div>
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe632;</span>
      输入景点/门票/游玩主题
    </div>
    <div class="header-right">
      城市
      <span class="iconfont">&#xe6aa;</span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeHeader'
}
</script>

<style lang="stylus" scoped>
  @import '~styles/variable.styl'
  .header
    display: flex
    line-height: .86rem
    background: $bgColor
    color: #fff
    .header-left
      width: .64rem
      float: left
      .back-icon
        text-align: center;
        font-size: .3rem;
    .header-input
      flex: 1
      height: .64rem
      line-height: .64rem
      background: #ff
      border-radius: .1rem
      margin-top: .12rem
      margin-left: .2rem
      color: #ccc
      padding-left: .2rem;
    .header-right
      width: 1.24rem
      float: right
      text-align: center
      margin-left: -0.06rem;
</style>
