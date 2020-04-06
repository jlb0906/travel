<template>
  <div class="wrapper">
    <swiper ref="mySwiper" :options="swiperOptions">
      <swiper-slide v-for="item of swiperList" :key="item.id">
        <img
          class="swiper-img"
          alt
          :src="item.imgUrl"
        />
      </swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data () {
    return { swiperOptions: {
      pagination: '.swiper-pagination',
      loop: true
    },
    swiperList: [
      {
        id: '001',
        imgUrl: '//imgs.qunarzz.com/p/tts0/1805/75/b55a998cd1cbac02.jpg_r_480x320x95_951a0d9c.jpg'
      },
      {
        id: '002',
        imgUrl: '//imgs.qunarzz.com/vs_ceph_vs_tts/21c70f4b-122b-4aa6-832a-88690a189a3b.jpg_r_480x320x95_ac8a583b.jpg'
      },
      {
        id: '003',
        imgUrl: '//imgs.qunarzz.com/vs_ceph_vs_tts/b12bffd0-3bb8-45df-b181-10adc5a9dfe7.jpg_r_480x320x95_85df1b64.jpg'
      }
    ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="stylus" scoped>
  .wrapper >>> .swiper-pagination-bullet-active
    background #fff
  .wrapper
    width 100%
    overflow hidden
    height 0
    padding-bottom 31.25%
    .swiper-img
      width 100%
      height 2.6rem
</style>
