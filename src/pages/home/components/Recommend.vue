<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
        <img class="item-img" :src="item.imgUrl" alt="" srcset="">
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-btn">查看详情</button>
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
      recommendList: [
        {
          id: '001',
          imgUrl: '//img1.qunarzz.com/sight/p0/1702/db/dbc8f6cf051b3803a3.water.jpg_256x160_0cff5839.jpg',
          title: '龙虎山',
          desc: '神秘的古越族文明，体验绝美的自然风光神秘的古越族文明'
        },
        {
          id: '002',
          imgUrl: '//img1.qunarzz.com/sight/p0/1702/db/dbc8f6cf051b3803a3.water.jpg_256x160_0cff5839.jpg',
          title: '龙虎山',
          desc: '神秘的古越族文明，体验绝美的自然风光神秘的古越族文明'
        },
        {
          id: '003',
          imgUrl: '//img1.qunarzz.com/sight/p0/1702/db/dbc8f6cf051b3803a3.water.jpg_256x160_0cff5839.jpg',
          title: '龙虎山',
          desc: '神秘的古越族文明，体验绝美的自然风光神秘的古越族文明'
        }
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="stylus" scoped>
@import '~@/assets/styles/mixins.style'
  .title
    line-height .8rem
    background #eee
    text-indent .2rem
    margin-top .2rem
  .item
    display flex
    height 1.9rem
    overflow hidden
    .item-img
      width 1.7rem
      height 1.7rem
      padding .1rem
    .item-info
      flex 1
      padding .1rem
      min-width 0
      .item-title
        line-height .54rem
        font-size .32rem
        ellipsis()
      .item-desc
        line-height .4rem
        color #ccc
        ellipsis()
      .item-btn
        background #ff9300
        padding 0 .2rem
        border-radius .06rem
        margin-top .16rem
        color #fff
        line-height .44rem

</style>
