<template>
  <div class="icons">
   <swiper ref="mySwiper" :options="swiperOptions">
      <swiper-slide v-for="(page, index) of pages" :key="index">
        <div class="icon" v-for="item of page" :key="item.id">
           <div class="icon-img">
            <img class="icon-img-content" :src="item.imgUrl">
          </div>
          <p class="icon-desc">{{item.desc}}</p>
        </div>
      </swiper-slide>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeIcons',
  data () {
    return {
      swiperOptions: {},
      iconsList: [
        {
          id: '001',
          imgUrl: '//s.qunarzz.com/homenode/images/touchheader/hotel.png',
          desc: '酒店'
        },
        {
          id: '002',
          imgUrl: '//s.qunarzz.com/homenode/images/touchheader/flight.png',
          desc: '机票'
        },
        {
          id: '003',
          imgUrl: '//s.qunarzz.com/homenode/images/touchheader/train.png',
          desc: '火车票'
        },
        {
          id: '004',
          imgUrl: '//s.qunarzz.com/homenode/images/touchheader/package.png',
          desc: '度假'
        },
        {
          id: '005',
          imgUrl: '//s.qunarzz.com/homenode/images/touchheader/hotel.png',
          desc: '酒店'
        },
        {
          id: '006',
          imgUrl: '//s.qunarzz.com/homenode/images/touchheader/flight.png',
          desc: '机票'
        },
        {
          id: '007',
          imgUrl: '//s.qunarzz.com/homenode/images/touchheader/train.png',
          desc: '火车票'
        },
        {
          id: '008',
          imgUrl: '//s.qunarzz.com/homenode/images/touchheader/package.png',
          desc: '度假'
        },
        {
          id: '009',
          imgUrl: '//s.qunarzz.com/homenode/images/touchheader/package.png',
          desc: '度假'
        },
        {
          id: '010',
          imgUrl: '//s.qunarzz.com/homenode/images/touchheader/package.png',
          desc: '度假度假度假度假度假度假'
        }
      ]
    }
  },
  computed: {
    pages () {
      const pages = []
      this.iconsList.forEach((item, index) => {
        const page = Math.floor(index / 8)
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(item)
      })
      return pages
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="stylus" scoped>
@import '~@/assets/styles/varibles.style'
@import '~@/assets/styles/mixins.style'
  .icons >>> .swiper-container
    height 0
    padding-bottom 50%
  .icons
    overflow hidden
    height 0
    padding-bottom 50%
    .icon
      position relative
      float left
      width 25%
      padding-bottom 25%
      height 0
      .icon-img
        position absolute
        top 0
        left 0
        right 0
        bottom .44rem
        box-box-sizing border-box
        padding .1rem
        .icon-img-content
          display block
          margin 0 auto
          height 100%
      .icon-desc
        position absolute
        left 0
        right 0
        bottom 0
        height .44rem
        line-height .44rem
        text-align center
        color $darkTextColor
        ellipsis()
</style>
