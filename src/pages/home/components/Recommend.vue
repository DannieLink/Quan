<template>
  <div>
  <div class="title">热销推荐</div>
    <ul>
      <router-link
        tag="li"
        class="item border-bottom"
        v-for="item of list"
        :key="item.id"
        :to=" '/detail/' +item.id">
          <img class="item-img" :src="item.imgUrl" >
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
export default {
  name: 'HomeRecommend',
  props: {
    list: Array
  }
}
// data () {
//   return {
//     recommendList: [{
//       id: '0001',
//       imgUrl: 'http://img1.qunarzz.com/sight/p0/1603/d7/d723cc2f4c7f459990.water.jpg_200x200_871f895b.jpg',
//       title: '四明山森林公园',
//       desc: '山中瑶草今人识，洞里桃花更盛开'
//     }, {
//       id: '0002',
//       imgUrl: 'http://img1.qunarzz.com/sight/p0/1603/37/37b8877cd2c8055e90.water.jpg_200x200_faf644e9.jpg',
//       title: '慈城古县城',
//       desc: '山中瑶草今人识，洞里桃花更盛开'
//     }, {
//       id: '0003',
//       imgUrl: 'http://img1.qunarzz.com/sight/p0/201301/08/08d4928f58459a5993835fbb.jpg_200x200_280c5bae.jpg',
//       title: '伍山石窟度假区',
//       desc: '山中瑶草今人识，洞里桃花更盛开'
//     }, {
//       id: '0004',
//       imgUrl: 'http://img1.qunarzz.com/sight/p0/1603/b6/b60b5c3acd9845de90.water.jpg_200x200_362a96e9.jpg',
//       title: '东钱湖',
//       desc: '东尽观沧海，往事一慨然'
//     }, {
//       id: '0005',
//       imgUrl: 'http://img1.qunarzz.com/sight/p0/1603/b6/b60b5c3acd9845de90.water.jpg_200x200_362a96e9.jpg',
//       title: '东钱湖',
//       desc: '东尽观沧海，往事一慨然'
//     }, {
//       id: '0006',
//       imgUrl: 'http://img1.qunarzz.com/sight/p0/1604/a8/a81673c5f10d323290.water.jpg_200x200_29e239f2.jpg',
//       title: '浙东小九寨',
//       desc: '东尽观沧海，往事一慨然'
//     }, {
//       id: '0007',
//       imgUrl: 'http://img1.qunarzz.com/sight/p0/1609/33/33d5213b34b64fdfa3.img.jpg_200x200_e0c93fa8.jpg',
//       title: '宁波植物园',
//       desc: '东尽观沧海，往事一慨然'
//     }, {
//       id: '0008',
//       imgUrl: 'http://img1.qunarzz.com/sight/p0/201212/14/cf7786f6c7627bc593835fbb.jpg_200x200_7730a1c0.jpg',
//       title: '宁波九龙湖',
//       desc: '东尽观沧海，往事一慨然'
//     }, {
//       id: '0009',
//       imgUrl: 'http://img1.qunarzz.com/sight/p0/1806/86/869c51673a5b17c4a3.water.jpg_200x200_4fbcd180.jpg',
//       title: '中国海影城 海上传奇',
//       desc: '宁波本月收藏Top5╰(￣▽￣)╭'
//     }, {
//       id: '00010',
//       imgUrl: 'http://img1.qunarzz.com/sight/p0/201405/23/9878029ca513c02652ee26bfe61a5799.jpg_200x200_07747d07.jpg',
//       title: '松兰山',
//       desc: '宁波本月收藏Top5╰(￣▽￣)╭'
//     }]
//   }
// }
</script>
<style lang="stylus" scoped>
  @import "~styles/mixins.styl"
  .title
    margin-top .2rem
    line-height .8rem
    background #eee
    text-indent .2rem
  .item
    overflow hidden
    display flex
    height 1.9rem
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
      color #ccc
      ellipsis()
    .item-button
      line-height .44rem
      margin-top .16rem
      background #ff9300
      padding 0.2rem
      border-radius .06rem
      color #fff
</style>
