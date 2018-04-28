<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
      <swiper-slide v-for="item in swiperList" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl">
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
      swiperList: [{
        id: '0001',
        imgUrl: 'https://img1.qunarzz.com/p/tts5/1612/4c/e30e710017cef102.jpg_r_1280x840x90_6809ec1f.jpg'
      }, {
        id: '0002',
        imgUrl: 'https://img1.qunarzz.com/p/tts2/1612/8e/865e9503f1615002.jpg_r_1280x840x90_1bca4455.jpg'
      }]
    }
  }
}
</script>

<style lang='stylus' scoped>
.wrapper >>> .swiper-pagination-bullet-active
  background-color : #FFF
.wrapper
  width: 100%
  height:0
  overflow: hidden
  padding-bottom: 66%
  background-color: #F5F5F5
  .swiper-img
    width: 100%
</style>
