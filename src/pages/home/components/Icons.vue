<template>
  <div class="icons">
    <swiper ref="mySwiper" :options="swiperOptions">
      <swiper-slide v-for="(page, index) of pages" :key="index">
        <div class="icon" v-for="item of page" :key="item.id">
          <div class="icon-img">
            <img class="icon-img-content" :src="item.imgUrl" />
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
  props: {
    list: Array
  },
  data () {
    return {
      swiperOptions: {
        autoplay: false
      }
    }
  },
  computed: {
    pages () {
      const pages = []
      this.list.forEach((item, index) => {
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
@import '~@/assets/styles/varibles.style';
@import '~@/assets/styles/mixins.style';

.icons >>> .swiper-container {
  height: 0;
  padding-bottom: 50%;
}

.icons {
  margin-top: 0.1rem;
  overflow: hidden;
  height: 0;
  padding-bottom: 50%;

  .icon {
    position: relative;
    float: left;
    width: 25%;
    padding-bottom: 25%;
    height: 0;

    .icon-img {
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      bottom: 0.44rem;
      box-box-sizing: border-box;
      padding: 0.1rem;

      .icon-img-content {
        display: block;
        margin: 0 auto;
        height: 100%;
      }
    }

    .icon-desc {
      position: absolute;
      left: 0;
      right: 0;
      bottom: 0;
      height: 0.44rem;
      line-height: 0.44rem;
      text-align: center;
      color: $darkTextColor;
      ellipsis();
    }
  }
}
</style>
