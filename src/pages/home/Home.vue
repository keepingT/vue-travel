<template>
  <!-- 模板最外层需要一个标签包裹 -->
  <div>
    <home-header></home-header>
    <home-swiper></home-swiper>
    <my-home-icons></my-home-icons>
  </div>
</template>

<script>
import HomeHeader from './components/Header'
import HomeSwiper from './components/Swiper'
import HomeIcons from './components/Icons'
export default {
  // name 为组件名
  name: 'Home',
  components: {
    // HomeHeader定义组件的标签名<home-header>
    HomeHeader,
    HomeSwiper,
    myHomeIcons: HomeIcons
  }
}
</script>

<style>

</style>
