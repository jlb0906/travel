<template>
  <div class="list" ref="wrapper">
    <div>

      <div class="area">
        <div class="title border-topbottom">当前城市</div>
        <div class="button-list">
          <div class="button-wrapper">
            <div class="button">北京</div>
          </div>
        </div>
      </div>
      <div class="area">
        <div class="title border-topbottom">热门城市</div>
              <div class="button-list">
          <div class="button-wrapper">
            <div class="button">北京</div>
          </div>
          <div class="button-wrapper">
            <div class="button">北京</div>
          </div>
          <div class="button-wrapper">
            <div class="button">北京</div>
          </div>
          <div class="button-wrapper">
            <div class="button">北京</div>
          </div>
          <div class="button-wrapper">
            <div class="button">北京</div>
          </div>
          <div class="button-wrapper">
            <div class="button">北京</div>
          </div>
        </div>
      </div>
      <div class="area">
        <div class="title border-topbottom">A</div>
        <div class="item-list">
          <div class="item border-bottom">阿莉尔</div>
          <div class="item border-bottom">阿莉尔</div>
          <div class="item border-bottom">阿莉尔</div>
        </div>
      </div>
      <div class="area">
        <div class="title border-topbottom">A</div>
        <div class="item-list">
          <div class="item border-bottom">阿莉尔</div>
          <div class="item border-bottom">阿莉尔</div>
          <div class="item border-bottom">阿莉尔</div>
        </div>
      </div>
      <div class="area">
        <div class="title border-topbottom">A</div>
        <div class="item-list">
          <div class="item border-bottom">阿莉尔</div>
          <div class="item border-bottom">阿莉尔</div>
          <div class="item border-bottom">阿莉尔</div>
        </div>
      </div>
      <div class="area">
        <div class="title border-topbottom">A</div>
        <div class="item-list">
          <div class="item border-bottom">阿莉尔</div>
          <div class="item border-bottom">阿莉尔</div>
          <div class="item border-bottom">阿莉尔</div>
        </div>
      </div>
      <div class="area">
        <div class="title border-topbottom">A</div>
        <div class="item-list">
          <div class="item border-bottom">阿莉尔</div>
          <div class="item border-bottom">阿莉尔</div>
          <div class="item border-bottom">阿莉尔</div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import BScroll from 'better-scroll'

export default {
  name: 'CityList',
  mounted () {
    this.scroll = new BScroll(this.$refs.wrapper)
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="stylus" scoped>
@import '~@/assets/styles/varibles.style';

.list {
  position absolute
  top 1.58rem
  left 0
  bottom 0
  right 0
  overflow hidden

  .title {
    background: #eee;
    color: #666;
    padding-left: 0.2rem;
    line-height: 0.54rem;
    font-size: 0.26rem;
  }

  .border-topbottom {
    &:before {
      border-color: #ccc;
    }

    &:after {
      border-color: #ccc;
    }
  }

  .border-topbottom {
    &:before {
      border-color: #ccc;
    }

    &:after {
      border-color: #ccc;
    }
  }

  .button-list {
    padding: .1rem .6rem .1rem .1rem;
    overflow hidden

    .button-wrapper {
      float left
      width 33.33%
      .button {
        margin .1rem
        text-align center
        border .02rem solid #ccc
        padding .1rem 0
        border-radius .06rem
      }
    }
  }

  .item-list {
    .item {
      line-height .76rem
      color #666
      padding-left .2rem
    }
  }
}
</style>
