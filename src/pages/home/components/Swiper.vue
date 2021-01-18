<template>
  <div class="wrapper">
    <!-- 如果不判断 if 是否为空时，则list为空数组时swiper会被创建，然后再动态加载后面 ajax 的数据，页数会显示为最后一页 -->
    <swiper :options="swiperOption" v-if="showSwiper">
      <swiper-slide v-for="item of list" :key="item.id">
        <img class="swiper-img" :src="item.imgUrl" />
      </swiper-slide>
      <div class="swiper-pagination" slot="pagination"></div>
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
        autoplay: 3000,
        loop: true
      }
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
