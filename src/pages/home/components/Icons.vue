<template>
  <div class="icons">
    <swiper :options="swiperOption">
      <swiper-slide v-for="(page, index) of pages" :key="index">
        <div class="icon"
          v-for="item of page"
          :key="item.id"
        >
          <div class="icon-img">
            <img class="icon-img-content" :src="item.imgUrl">
          </div>
          <p class="icon-desc">{{item.desc}}</p>
        </div>
      </swiper-slide>
      </swiper>
  </div>
</template>

<script>
export default{
  name: 'HomeIcon',
  data () {
    return {
      swiperOption: {
      },
      iconList: [{
        id: '0001',
        imgUrl: 'https://dummyimage.com/100x100/739bde/fff',
        desc: '景点门票'
      }, {
        id: '0002',
        imgUrl: 'https://dummyimage.com/100x100/73d6de/fff',
        desc: '滑雪季'
      }, {
        id: '0003',
        imgUrl: 'https://dummyimage.com/100x100/73d6de/fff',
        desc: '泡温泉'
      }, {
        id: '0004',
        imgUrl: 'https://dummyimage.com/100x100/73d6de/fff',
        desc: '动植物园'
      }, {
        id: '0005',
        imgUrl: 'https://dummyimage.com/100x100/739bde/fff',
        desc: '景点门票'
      }, {
        id: '0006',
        imgUrl: 'https://dummyimage.com/100x100/73d6de/fff',
        desc: '滑雪季'
      }, {
        id: '0007',
        imgUrl: 'https://dummyimage.com/100x100/73d6de/fff',
        desc: '泡温泉'
      }, {
        id: '0008',
        imgUrl: 'https://dummyimage.com/100x100/73d6de/fff',
        desc: '动植物园'
      }, {
        id: '0009',
        imgUrl: 'https://dummyimage.com/100x100/73d6de/fff',
        desc: '动植物园'
      }]
    }
  },
  computed: {
    pages () {
      const pages = []
      this.iconList.forEach((item, index) => {
        const page = Math.floor(index / 8)
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(item)
      })
      return pages
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/varibles.styl'
  @import '~styles/mixins.styl'
  .icons >>> .swiper-container
    overflow: hidden
    height: 0
    padding-bottom: 50%
  .icons
    margin-top: .1rem
    .icon
      position: relative
      overflow: hidden
      float: left
      height: 0
      width: 25%
      padding-bottom: 25%
      .icon-img
        position: absolute
        top: 0
        left: 10%
        right: 10%
        bottom: .44rem
        box-sizing: border-box
        padding: .1rem
        .icon-img-content
          height: 100%
          width: 100%
      .icon-desc
        position: absolute
        left: 0
        right: 0
        bottom: 0
        height: .44rem
        line-height: .44rem
        text-align: center
        color: $darkText
        ellipsis()
</style>
