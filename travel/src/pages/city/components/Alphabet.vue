<template>
  <div class="list">
    <div class="item" v-for="(item, key) in cities" :key="key" @click="handleLetterClick">{{key}}</div>
  </div>
</template>

<script>
export default {
  name: 'CityAlphabet',
  props: {
    cities: Object
  },
  methods: {
    handleLetterClick (e) {
      this.$emit('change', e.target.innerText)
    }
  }
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
      padding: .05rem
</style>
