<template>
  <div>
  	<div class="title">热销推荐</div>
  	<ul>
  		<li class="item border-bottom" v-for="item of recommendList" :key="item.id">
	  		<img class="item-img" :src="item.imgUrl"></img>
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
				imgUrl: 'http://img1.qunarzz.com/sight/p0/2101/33/334d60ba3ae91776a3.img.jpg_200x200_263e96c3.jpg',
				title: '长隆欢乐世界',
				desc: '垂直过山车等挑战你的青春荷尔蒙'
			}, {
				id: '0002',
				imgUrl: 'http://img1.qunarzz.com/sight/p0/2001/78/78cf0b84b66945da3.img.png_256x160_4ba28598.png',
				title: '长鹿旅游休博园',
				desc: '体验岭南历史文化，感受农家生活情趣'
			}, {
				id: '0003',
				imgUrl: 'https://img1.qunarzz.com/sight/p0/201403/04/abf9d2133fbfc65ac5d7d15eebebd374.jpg_256x160_926aa4f1.jpg',
				title: '锦绣中华民俗村',
				desc: '深圳小人国——实景微缩景区候选世界纪录'
			}]
		}
	}
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl'
  .title
    margin-top: .2rem
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
    	min-width: 0;
    	.item-title
    		line-height: .54rem
    		font-size: .32rem
    		ellipsis()
    	.item-desc
    		line-height: .4rem
    		color: #ccc
    		ellipsis()
    	.item-button
    		line-height: .44rem
    		background: #ff9300
    		padding: 0 .2rem
    		border-radius: .06rem
    		margin-top: .16rem
    		color: #fff
</style>