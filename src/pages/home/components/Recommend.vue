<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
      <li class="item border-bottom"
          v-for="item of recomendList"
          :key="item.id"
      >
        <img class="item-img"
             :src="item.imgUrl">
        <div class="item-info">
          <p class="item-title">{{ item.tilte }}</p>
          <p class="item-desc">{{item.desc}}</p>
          <button class="item-button">查看详情</button>
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
      recomendList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/201307/15/7eab0785f2aa37e8c8d65eac.jpg_200x200_ca7ce0e0.jpg',
        tilte: '大梅沙',
        desc: '大梅沙海滨公园位于深圳特区东部，地处南海之滨。'
      },
      {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1505/c6/c6277b512fd15c8b.water.jpg_200x200_2fd4e290.jpg',
        tilte: '玫瑰海岸旅游度假区',
        desc: '玫瑰海岸是大鹏湾内的一处绝美海滩，这里沙平水清，海岸上拥有众多城堡、花海等梦幻场景，从而成为了深圳热门的婚纱摄影地。'
      },
      {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/2203/62/62bb1f47f6146658a3.water.jpg_200x200_d55fce9a.jpg',
        tilte: '世界之窗',
        desc: '景区按世界地域结构和游览活动内容分为世界广场、亚洲区、大洋洲区、欧洲区、非洲区、美洲区、雕塑园区、国际街。'
      }
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
@import "~styles/mixins.styl"

.title
  margin-top: .2rem
  line-height: .8rem
  background: #eee
  text-indent: .2rem
  color : #212121

.item
  overflow: hidden
  display: flex
  height: 1.9rem

  .item-img
    width: 1.7rem
    heighit: 1.7rem
    padding: .1rem

  .item-info
    flex: 1
    padding: .1rem
    min-width: 0

    .item-title
      line-height: .54rem
      font-size: .32rem
      ellipsis()

    .item-desc
      line-height: .4rem
      color: #ccc
      ellipsis()

    .item-button
      line-height: .44rem
      margin-top: .16rem
      background: #ff9300
      border-radius: .06rem
</style>
