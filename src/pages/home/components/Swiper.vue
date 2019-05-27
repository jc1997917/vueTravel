<template>
  <div class="wrapper">
    <swiper :options="swiperOption">
        <swiper-slide v-for="item of swiperList" :key="item.id">
          <img class="swiper-img" :src="item.imgUrl">
        </swiper-slide>
        <div class="swiper-pagination"  slot="pagination"></div>
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
        imgUrl: '//imgs.qunarzz.com/p/tts6/1905/a0/b80e850f81af4902.jpg_256x144_b99508a4.jpg'
      },{
        id: '0002',
        imgUrl: '//imgs.qunarzz.com/p/tts9/1901/38/348a22b45e8c0102.png_256x144_ef444c86.png'
      },
      {
        id: '0003',
        imgUrl: '//imgs.qunarzz.com/p/tts1/1904/e1/a7958dfaeade1b02.jpg_256x144_04d3028b.jpg'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  .wrapper >>> .swiper-pagination-bullet-active
    background: #fff
  .wrapper
    width: 100%
    height: 56.28vw
    background: #eee
    .swiper-img
      width: 100%
      height: 100%
</style>
