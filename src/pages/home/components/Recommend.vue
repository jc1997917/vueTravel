<template>
  <div>
      <div class="recommend-title">热销推荐</div>
      <ul>
          <router-link
          tag="li"
          class="item border-bottom"
          v-for="item of list"
          :key="item.id"
          :to="'/detail/' + item.id"
          >
            <img class="item-img" :src="item.imgUrl">
            <div class="item-info">
              <p class="item-title">{{item.title}}</p>
              <p class="item-desc">{{item.desc}}</p>
              <button class="item-button">查看详情</button>
            </div>
          </router-link>
      </ul>
  </div>
</template>

<script>
export default{
  name: 'HomeRecommend',
  props: {
    list: Array
  },
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'https://dummyimage.com/100x100/64ff66/fff',
        title: '北京-泰国 7天自由行',
        desc: '519大促！泰国普吉岛「芭东区海边酒店」机酒+赠专车接送机+保险+赠流量卡'
      }, {
        id: '0002',
        imgUrl: 'https://dummyimage.com/100x100/64ff66/fff',
        title: '北京-泰国 7天自由行',
        desc: '519大促！泰国普吉岛「芭东区海边酒店」机酒+赠专车接送机+保险+赠流量卡'
      }, {
        id: '0003',
        imgUrl: 'https://dummyimage.com/100x100/64ff66/fff',
        title: '北京-泰国 7天自由行',
        desc: '519大促！泰国普吉岛「芭东区海边酒店」机酒+赠专车接送机+保险+赠流量卡'
      }, {
        id: '0004',
        imgUrl: 'https://dummyimage.com/100x100/64ff66/fff',
        title: '北京-泰国 7天自由行',
        desc: '519大促！泰国普吉岛「芭东区海边酒店」机酒+赠专车接送机+保险+赠流量卡'
      }, {
        id: '0005',
        imgUrl: 'https://dummyimage.com/100x100/64ff66/fff',
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
    line-height: .8rem
    background: #eee
    text-indent: .2rem
  .item
    overflow: hidden
    display: flex
    height: 1.9rem
    .item-img
      width: 1.7rem
      height: 1.7rem
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
        color #ccc
        ellipsis()
      .item-button
        line-height: .44rem
        margin-top: .16rem
        background: #ff9300
        padding: 0 .2rem
        border-radius: .1rem
        color: #fff
</style>
