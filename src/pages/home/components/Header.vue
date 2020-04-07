<template>
  <div class="header">
    <div class="header-left">
      <div class="iconfont iconfanhui back-icon"></div>
    </div>
    <div class="header-input">
      <span class="iconfont iconsousuo"></span> 请输入游玩景点
    </div>
      <router-link to="/city">
        <div class="header-right">
            {{ this.city }}
            <span class="iconfont iconjiantouxia arrow-icon"></span>
        </div>
      </router-link>
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
@import '~@/assets/styles/varibles.style';

.header {
  display: flex;
  line-height: $headerHeight;
  background: $bgColor;
  color: #fff;

  .header-left {
    width: 0.64rem;
    float: left;

    .back-icon {
      text-align: center;
      font-size: 0.4rem;
    }
  }

  .header-input {
    flex: 1;
    background: #fff;
    border-radius: 0.1rem;
    margin-top: 0.12rem;
    margin-left: 0.2rem;
    height: 0.64rem;
    line-height: 0.64rem;
    color: #ccc;
    padding-left: 0.2rem;
  }

  .header-right {
    width: 1.24rem;
    float: right;
    text-align: center;
    color: #fff;

    .arrow-icon {
      font-size: 0.24rem;
      margin-left: 0.04rem;
    }
  }
}
</style>
