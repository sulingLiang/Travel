<template>
  <div class="list">
    <div class="item">A</div>
    <div class="item">A</div>
    <div class="item">A</div>
    <div class="item">A</div>
    <div class="item">A</div>
    <div class="item">A</div>
    <div class="item">A</div>
    <div class="item">A</div>
  </div>
</template>

<script>
export default {
  name: 'CityAlphabet'
}
</script>

<style lang="stylus" scoped>
  @import '~styles/variable.styl'
  .list
    position: absolute
    top: 1.58rem
    right: 0
    bottom: 0
    width: .4rem
    text-align: center
    display: flex
    align-items: center
    flex-direction: column
    justify-content: center
    .item
      color: $bgColor
</style>
