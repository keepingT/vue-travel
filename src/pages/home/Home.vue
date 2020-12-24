<template>
  <!-- 模板最外层需要一个标签包裹 -->
  <div>
    <home-header></home-header>
  </div>
</template>

<script>
import HomeHeader from './components/Header'
export default {
  // name 为组件名
  name: 'Home',
  components: {
    // HomeHeader定义组件的标签名<home-header>
    HomeHeader
  }
}
</script>

<style>

</style>
