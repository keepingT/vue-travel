<template>
  <div class="header">
    <div class="header-left">
      <div class="iconfont back-icon">&#xe612;</div>
    </div>
    <div class="header-input">
      <span class="iconfont">&#xe699;</span>
      输入城市/景点/游玩主题
    </div>
    <router-link to="/city">
      <div class="header-right">
        {{city}}
        <span class="iconfont arrow-icon">&#xe877;</span>
      </div>
    </router-link>
  </div>
</template>

<script>
export default {
  name: 'HomeHeader',
  props: {
    city: String
  }
}
</script>

<!-- lang定义使用的是什么类型的样式
scoped设置的样式只适用于该组件，会在DOM元素上添加一个data-v-xxxxxxxx属性，即利用css类选择 + 属性选择器实现，
如.header .header-input[data-v-5558831a]
 -->
<style lang="stylus" scoped>
// @import 引入样式需要添加@符号
// 在css中使用路径符号如@、styles需要在前添加波浪号~
  @import '~styles/variables.styl'
  .header
    line-height: .84rem
    background: $bgColor
    display: flex
    color: #fff
    .header-left
      float: left
      width: .64rem
      .back-icon
        text-align: center
        font-size: .4rem
    .header-input
      flex: 1
      background: #fff
      margin-top: .12rem
      padding-left: .2rem
      height .62rem
      line-height .62rem
      border-radius: .1rem
      color: #ccc
    .header-right
      float: right
      width: 1.24rem
      text-align: center
      color: #fff
      .arrow-icon
        margin-left: -.04rem
        font-size: .35rem
</style>
