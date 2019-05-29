<template>
  <div>
      <div class="recommend-title">周末去哪儿</div>
      <ul>
          <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
            <div class="item-img-wrapper">
              <img class="item-img" :src="item.imgUrl">
            </div>
            <div class="item-info">
              <p class="item-title">{{item.title}}</p>
              <p class="item-desc">{{item.desc}}</p>
            </div>
          </li>
      </ul>
  </div>
</template>

<script>
export default{
  name: 'HomeWeekend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'https://dummyimage.com/640x214/64fff6/fff',
        title: '北京-泰国 7天自由行',
        desc: '519大促！泰国普吉岛「芭东区海边酒店」机酒+赠专车接送机+保险+赠流量卡'
      }, {
        id: '0002',
        imgUrl: 'https://dummyimage.com/640x214/64fff6/fff',
        title: '北京-泰国 7天自由行',
        desc: '519大促！泰国普吉岛「芭东区海边酒店」机酒+赠专车接送机+保险+赠流量卡'
      }, {
        id: '0003',
        imgUrl: 'https://dummyimage.com/640x214/64fff6/fff',
        title: '北京-泰国 7天自由行',
        desc: '519大促！泰国普吉岛「芭东区海边酒店」机酒+赠专车接送机+保险+赠流量卡'
      }, {
        id: '0004',
        imgUrl: 'https://dummyimage.com/640x214/64fff6/fff',
        title: '北京-泰国 7天自由行',
        desc: '519大促！泰国普吉岛「芭东区海边酒店」机酒+赠专车接送机+保险+赠流量卡'
      }, {
        id: '0005',
        imgUrl: 'https://dummyimage.com/640x214/64fff6/fff',
        title: '北京-泰国 7天自由行',
        desc: '519大促！泰国普吉岛「芭东区海边酒店」机酒+赠专车接送机+保险+赠流量卡'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .recommend-title
    margin-top: .2rem
    line-height: .8rem
    background: #eee
    text-indent: .2rem
  .item-img-wrapper
    overflow: hidden
    height: 0
    padding-bottom: 33.9%
    .item-img
      width: 100%
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
      color #ccc
      ellipsis()
</style>
