<template>
  <div>
    <div class="title">周末去哪</div>
    <ul>
      <!--recommendList-->
      <li class="item border-bottom" v-for="item of list" :key="item.id">
        <div class="item-img-wrapper">
        <img class="item-img" :src="item.imgUrl" >
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
export default {
  name: 'HomeWeekend',
  props: {
    list: Array
  }
}
// data () {
//   return {
//     recommendList: [{
//       id: '0001',
//       imgUrl: 'http://img1.qunarzz.com/sight/source/1510/c1/afe3ab32b3bc23.jpg_r_640x214_beb61760.jpg',
//       title: '青山秀水，精致暖汤',
//       desc: '天然高品质温泉，这个冬天秀美容颜首选'
//     }, {
//       id: '0002',
//       imgUrl: 'http://img1.qunarzz.com/sight/source/1811/52/b6776b49d27025.jpg_r_640x214_35ae205c.jpg',
//       title: '美丽普陀山',
//       desc: '人间仙境杭州，佛教圣地普陀山等你来玩！'
//     }, {
//       id: '0003',
//       imgUrl: 'http://img1.qunarzz.com/sight/source/1509/fb/c45a951a9b4305.jpg_r_640x214_26fcfd26.jpg',
//       title: '温州动人秋色',
//       desc: '细数温州那些美到陶醉的赏秋地'
//     }, {
//       id: '0004',
//       imgUrl: 'http://img1.qunarzz.com/sight/source/1505/65/70e96eb29d7ea5.jpg_r_640x214_2df4cbcd.jpg',
//       title: '最爱的温泉',
//       desc: '边泡边欣赏外面的风景，幸福满满'
//     }, {
//       id: '0005',
//       imgUrl: 'http://img1.qunarzz.com/sight/source/1509/2b/5844bf97c9c59.jpg_r_640x214_d932f6a0.jpg',
//       title: '赏秋好时节',
//       desc: '泛黄的银杏正值茂盛，沿路风景美不胜收'
//     }]
//   }
// }

</script>
<style lang="stylus" scoped>
  @import "~styles/mixins.styl"
  .title
    line-height .8rem
    background #eee
    text-indent .2rem
  .item-img-wrapper
    overflow hidden
    height 0
    padding-bottom 37.09%
   .item-img
     width 100%
  .item-info
    padding .1rem
  .item-title
    line-height .54rem
    font-size .32rem
    ellipsis()
  .item-desc
    line-height .4rem
    color #ccc
    ellipsis()

</style>
