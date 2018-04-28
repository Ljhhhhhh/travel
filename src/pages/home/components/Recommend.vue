<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
      <li
      class="item border-bottom"
      v-for="item of recommendList"
      :key="item.id"
      >
        <img class="item-img" :src="item.imgUrl">
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
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
      recommendList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1706/cd/cd76ff0dcb161728a3.img.jpg_200x200_36d3c8a5.jpg',
        title: '横店秦王宫',
        desc: '这里最近很火哦，好多人都在点评它呢！'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1706/31/31c2360540d09d58a3.water.jpg_200x200_5f6631fa.jpg',
        title: '横店影视城',
        desc: '这里最近很火哦，好多人都在点评它呢！'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/201301/05/a2b6b90239ae74e193835fbb.png_200x200_c6d3d687.png',
        title: '武义牛头山国家森林公园',
        desc: '这里最近很火哦，好多人都在点评它呢！'
      }, {
        id: '0004',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/201301/16/ede0c90f7a92082a93835fbb.jpg_200x200_7c5cf1ee.jpg',
        title: '义乌海洋世界',
        desc: '这里最近很火哦，好多人都在点评它呢！'
      }, {
        id: '0005',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1603/3b/3bf72068b9e244fd90.water.jpg_200x200_656f68e1.jpg',
        title: '诸葛八卦村',
        desc: '这里最近很火哦，好多人都在点评它呢！'
      }, {
        id: '0006',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1706/28/28b983d7d93559a6a3.img.jpg_200x200_fcc59314.jpg',
        title: '横店梦幻谷',
        desc: '这里最近很火哦，好多人都在点评它呢！'
      }, {
        id: '0007',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1611/e5/e5d83162ca7a89f1a3.water.jpg_200x200_51ca5c86.jpg',
        title: '金华浙中乐园',
        desc: '这里最近很火哦，好多人都在点评它呢！'
      }, {
        id: '0008',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1603/50/5020c11e7dde947390.water.jpg_200x200_a7b59471.jpg',
        title: '清水湾沁温泉',
        desc: '这里最近很火哦，好多人都在点评它呢！'
      }]
    }
  }
}
</script>
<style lang="stylus" scoped>
  @import '~styles/mixins.styl';
  .title
    margin-top .2rem
    line-height .8rem
    background #EEE
    text-indent .2rem
  .item
    display flex
    height 1.9rem
    overflow hidden
    .item-img
      width 1.7rem
      height 1.7rem
      padding .1rem
    .item-info
      flex 1
      padding .1rem
      min-width 0
      .item-title
        line-height .54rem
        font-size .32rem
        ellipsis()
      .item-desc
        line-height .4rem
        color #CCC
        ellipsis()
      .item-button
        margin-top .16rem
        background #ff9300
        padding 0 .2rem
        border-radius .06rem
        color #fff
</style>
