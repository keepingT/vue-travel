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
        autoplay: 3000,
        loop: true
      },
      swiperList: [{
        id: '0001',
        imgUrl: 'https://imgs.qunarzz.com/vs_ceph_vcimg/569cae4ae98e9793f7341e85eed73c54.jpeg'
      }, {
        id: '002',
        imgUrl: 'https://imgs.qunarzz.com/vs_ceph_vcimg/f7813c9431796cc32ae7b7a78447342e.jpeg'
      }, {
        id: '003',
        imgUrl: 'https://imgs.qunarzz.com/vs_ceph_vcimg/569cae4ae98e9793f7341e85eed73c54.jpeg'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  .wrapper >>> .swiper-pagination-bullet-active
    background: #fff
  .wrapper
    //---设置高度，防止图片高度从无到有的抖动，该方式适用于高度不定的情况---start
    overflow: hidden
    width: 100%
    //该高度是相对于父级的高度，所以不能设置height
    height: 0
    //轮播的图片宽高比为100：31.25,所以设置padding-bottom为百分比，实现高度为31.25%
    padding-bottom: 31.25%
    //---设置高度，防止图片高度从零到有的抖动---end
    .swiper-img
      width: 100%
</style>
