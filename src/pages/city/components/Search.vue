<template>
  <div>
    <div class="search">
      <input v-model="keyword" type="text" class="search-input" placeholder="输入城市名">
    </div>

    <div class="search-content" ref="search" v-show="keyword">
      <ul>
        <li v-for="(item, index) of list" :key="index" class="search-item border-bottom">{{item.name}}</li>
        <li class="search-item border-bottom" v-show="!list.length">没有找到匹配数据</li>
      </ul>
    </div>
  </div>
</template>

<script>
import Bscroll from 'better-scroll'
export default {
  name: 'CitySearch',
  data () {
    return {
      keyword: '',
      list: [],
      timer: null
    }
  },
  props: {
    cities: Object
  },
  watch: {
    keyword () {
      if (this.timer) {
        clearTimeout(this.timer)
      }
      if (!this.keyword) {
        this.list = []
        return
      }
      this.timer = setTimeout(() => {
        const result = []
        for (let i in this.cities) {
          this.cities[i].forEach(element => {
            if (element.spell.indexOf(this.keyword) > -1 ||
            element.name.indexOf(this.keyword) > -1) {
              result.push(element)
            }
          })
          this.list = result
        }
      }, 100)
    }
  },
  mounted () {
    this.scroll = new Bscroll(this.$refs.search)
  }
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
.search-content
  position absolute
  overflow hidden
  z-index 1
  top 1.58rem
  left 0
  right 0
  bottom 0
  .search-item
    line-height .62rem
    padding-left .2rem
    color #666
    background #fff
</style>
