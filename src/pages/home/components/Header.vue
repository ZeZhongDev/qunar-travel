<template>
  <div class="header">
    <div class="header-left">
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe632;</span>
      输入城市/景点/游玩主题
    </div>
    <router-link to="/city">
      <div class="header-right">
        <span class="iconfont arrow-icon">&#xe64a;</span>
        {{ this.city }}
      </div>
    </router-link>
  </div>

</template>

<script>
import {mapState} from 'vuex'

export default {
  name: 'HomeHeader',
  computed: {
    ...mapState(['city'])
  }
}
</script>

<style lang="stylus" scoped>
@import "~styles/varibles.styl"
.header
  display: flex
  line-height: 1rem
  background-color: #ffffff
  background-color: $bgColor

  .header-left
    width: .24rem
    float: left

  .header-input
    flex: 1
    height: .64rem
    line-height: .64rem
    margin-top: .18rem
    margin-left: .2rem
    padding-left: .2rem
    background-color: #ffffff
    //border-radius: .1rem
    border-radius: .32rem
    color: #999999

  .header-right
    min-width: 1.04rem
    padding: 0 .1rem
    float: right
    text-align: center
    color: #ffffff

    .arrow-icon
      margin-left: -.04rem
      font-size: .24rem
</style>
