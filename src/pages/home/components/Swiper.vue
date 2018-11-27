<template>
  <div class="wrapper">
    <swiper :options="swiperOption" v-if="showSwiper">
      <!--swiperList-->
        <swiper-slide v-for="item of list" :key="item.id">
          <img class="swiper-img" :src="item.imgUrl" >
        </swiper-slide>
      <div class="swiper-pagination"  slot="pagination"></div>
  </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  props: {
    list: Array
  },
  data () {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      }
      // swiperList: [{
      //   id: '0001',
      //   imgUrl: 'http://img1.qunarzz.com/piao/fusion/1811/31/da037478f37cf202.jpg_750x200_fe28d396.jpg'
      // }, {
      //   id: '0002',
      //   imgUrl: 'http://img1.qunarzz.com/piao/fusion/1811/4d/6706bf772c05ce02.jpg_750x200_773e75f0.jpg'
      // }, {
      //   id: '0003',
      //   imgUrl: 'http://img1.qunarzz.com/piao/fusion/1811/7c/8e5c4ab8ee8b7402.jpg_750x200_dd7a38dd.jpg'
      // }, {
      //   id: '0004',
      //   imgUrl: 'http://img1.qunarzz.com/piao/fusion/1711/61/0af7f65988570e02.jpg_750x200_905350d6.jpg'
      // }, {
      //   id: '0005',
      //   imgUrl: 'http://img1.qunarzz.com/piao/fusion/1811/c6/2467595fffc3b302.jpg_750x200_bc88db3a.jpg'
      // }, {
      //   id: '0006',
      //   imgUrl: 'http://img1.qunarzz.com/piao/fusion/1811/9d/a6e922acbb4c9802.jpg_750x200_74080b0c.jpg'
      // }]
    }
  },
  computed: {
    showSwiper () {
      return this.list.length
    }
  }
}
</script>

<style lang="stylus" scoped>
  .wrapper >>>.swiper-pagination-bullet-active
    background #fff !important
  .wrapper
        overflow hidden
      width 100%
      height 0
      padding-bottom 54.25%
      background #eee
    /*height 47.25vw*/
    .swiper-img
      width 100%
</style>
