<template>
  <div class="header">
    城市选择
    <router-link to="/">
      <div class="iconfont iconfanhui header-back"></div>
    </router-link>
  </div>
</template>

<script>
export default {
  name: 'CityHeader'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="stylus" scoped>
@import '~@/assets/styles/varibles.style';

.header {
  position: relative;
  overflow: hidden;
  height: $headerHeight;
  line-height: $headerHeight;
  text-align: center;
  color: #fff;
  background: $bgColor;
  font-size: 0.32rem;

  .header-back {
    width: 0.64rem;
    text-align: center;
    font-size: 0.4rem;
    position: absolute;
    top: 0;
    color: #fff;
  }
}
</style>
