<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
      <swiper-slide v-for="item of swiperList" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl" />
      </swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperList: [
        {
          id: '0001',
          imgUrl: 'https://imgs.qunarzz.com/vc/b2/cb/7e/478af3eeb2027d756756527494.jpg_92.jpg'
        },
        {
          id: '0002',
          imgUrl: 'https://imgs.qunarzz.com/vc/05/fd/d7/8e57c268866f4b89038baf267c.jpg_92.jpg'
        },
        {
          id: '0003',
          imgUrl: 'https://imgs.qunarzz.com/vc/80/ee/ae/5ae2ee75883e6339f0f167d420.jpg_92.jpg'
        }
      ]
    }
  }
}
</script>

<style lang="stylus" scoped>
.wrapper >>> .swiper-pagination-bullet-active
  background: #fff

.wrapper
  overflow :hidden
  height :0
  width : 100%
  padding-bottom : 24.89%
  background-color: #eee
  .swiper-img
    width: 100%
</style>
