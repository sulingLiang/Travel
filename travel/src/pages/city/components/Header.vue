<template>
  <div class="header">
    城市选择
    <router-link to="/">
      <div class="iconfont header-icon">&#xe624;</div>
    </router-link>
  </div>
</template>

<script>
export default {
  name: 'CityHeader'
}
</script>

<style lang="stylus" scoped>
  @import '~styles/variable.styl'
  .header
    position: relative
    height: $headeHeight
    line-height: $headeHeight
    text-align: center
    color: #fff
    font-size: .32rem
    background: $bgColor
    .header-icon
      position: absolute
      top: 0
      left: 0
      width: .7rem
      height: .77rem
      text-align: center
      font-size: .36rem
      color: #fff
</style>
