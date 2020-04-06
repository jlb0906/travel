<template>
  <div class="header">
     <div class="header-left">
       <div class="iconfont iconfanhui back-icon"></div>
     </div>
     <div class="header-input"><span class="iconfont iconsousuo"></span> 请输入游玩景点</div>
     <div class="header-right">{{this.city}}<span class="iconfont iconjiantouxia arrow-icon"></span></div>
  </div>
</template>

<script>
export default {
  name: 'HomeHeader',
  props: {
    city: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="stylus" scoped>
@import '~@/assets/styles/varibles.style'
  .header
    display flex
    line-height .86rem
    background $bgColor
    color #fff
    .header-left
      width .64rem
      float left
      .back-icon
        text-align center
        font-size .4rem
    .header-input
      flex 1
      background #fff
      border-radius .1rem
      margin-top .12rem
      margin-left .2rem
      height .64rem
      line-height .64rem
      color #ccc
      padding-left: .2rem
    .header-right
      width 1.24rem
      float right
      text-align center
      .arrow-icon
        font-size .24rem
        margin-left: .04rem
</style>
