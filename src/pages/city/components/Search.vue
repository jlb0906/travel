<template>
  <div class="search">
    <input type="text" class="search-input" placeholder="输入城市名">
  </div>
</template>

<script>
export default {
  name: 'CitySearch'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="stylus" scoped>
@import '~@/assets/styles/varibles.style';

.search
  background $bgColor
  height .72rem
  padding 0 .1rem

  .search-input
    height .62rem
    line-height .62rem
    text-align center
    width 100%
    border-radius .06rem
    color #666
    padding 0 .1rem
    box-sizing border-box
</style>
