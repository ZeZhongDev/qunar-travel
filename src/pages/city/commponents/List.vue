<template>
  <div class="list" ref="wrapper">
    <div class="content">
      <div class="area">
        <div class="title border-topbottom">当前城市</div>
        <div class="button-list">
          <div class="button-wrapper">
            <div class="button">深圳</div>
          </div>
        </div>
      </div>
      <div class="area">
        <div class="title border-topbottom">当前城市</div>
        <div class="button-list">
          <div class="button-wrapper">
            <div class="button">深圳</div>
          </div>
          <div class="button-wrapper">
            <div class="button">深圳</div>
          </div>
          <div class="button-wrapper">
            <div class="button">深圳</div>
          </div>
          <div class="button-wrapper">
            <div class="button">深圳</div>
          </div>
          <div class="button-wrapper">
            <div class="button">深圳</div>
          </div>
          <div class="button-wrapper">
            <div class="button">深圳</div>
          </div>
          <div class="button-wrapper">
            <div class="button">深圳</div>
          </div>
        </div>
      </div>
      <div class="area">
        <div class="title border-topbottom">
          A
        </div>
        <div class="item-list">
          <div class="item border-bottom">北京</div>
          <div class="item border-bottom">上海</div>
          <div class="item border-bottom">杭州</div>
          <div class="item border-bottom">广州</div>
        </div>
        <div class="title border-topbottom">
          B
        </div>
        <div class="item-list">
          <div class="item border-bottom">北京</div>
          <div class="item border-bottom">上海</div>
          <div class="item border-bottom">杭州</div>
          <div class="item border-bottom">广州</div>
        </div>
        <div class="title border-topbottom">
          C
        </div>
        <div class="item-list">
          <div class="item border-bottom">北京</div>
          <div class="item border-bottom">上海</div>
          <div class="item border-bottom">杭州</div>
          <div class="item border-bottom">广州</div>
        </div>
        <div class="title border-topbottom">
          D
        </div>
        <div class="item-list">
          <div class="item border-bottom">北京</div>
          <div class="item border-bottom">上海</div>
          <div class="item border-bottom">杭州</div>
          <div class="item border-bottom">广州</div>
        </div>
        <div class="title border-topbottom">
          E
        </div>
        <div class="item-list">
          <div class="item border-bottom">北京</div>
          <div class="item border-bottom">上海</div>
          <div class="item border-bottom">杭州</div>
          <div class="item border-bottom">广州</div>
        </div>
        <div class="title border-topbottom">
          E
        </div>
        <div class="item-list">
          <div class="item border-bottom">北京</div>
          <div class="item border-bottom">上海</div>
          <div class="item border-bottom">杭州</div>
          <div class="item border-bottom">广州</div>
        </div>
        <div class="title border-topbottom">
          F
        </div>
        <div class="item-list">
          <div class="item border-bottom">北京</div>
          <div class="item border-bottom">上海</div>
          <div class="item border-bottom">杭州</div>
          <div class="item border-bottom">广州</div>
        </div>
        <div class="title border-topbottom">
          H
        </div>
        <div class="item-list">
          <div class="item border-bottom">北京</div>
          <div class="item border-bottom">上海</div>
          <div class="item border-bottom">杭州</div>
          <div class="item border-bottom">广州</div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Bscroll from 'better-scroll'
export default {
  name: 'CityList',
  mounted () {
    this.scroll = new Bscroll(this.$refs.wrapper, {
      click: true
    })
  },
  updated () {
    this.scroll.refresh()
  }
}
</script>

<style lang="stylus" scoped>
.border-topbottom
  &:before
    border-color: #ccc

  &:after
    border-color: #ccc

.border-bottom
  &:before
    border-color: #ccc

.list
  overflow: hidden
  position: absolute
  top: 1.58rem
  left: 0
  right: 0
  bottom: 0

  .title
    line-height: .54rem
    background: #eaeaea
    padding-left: .2rem
    color: #666666
    font-size: .26rem

  .button-list
    overflow: hidden
    padding: .1rem .6rem .1rem .1rem

    .button-wrapper
      float: left
      width: 33.33%

      .button
        margin: .1rem
        pading: .1rem 0
        text-align: center
        border: .02rem solid #ccc
        border-radius: .06rem

  .item-list
    .item
      line-height: .54rem
      padding-left: .2rem
</style>
