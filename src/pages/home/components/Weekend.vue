<template>
  <div>
  	<div class="title">周末去哪儿</div>
  	<ul>
  		<li class="item border-bottom" v-for="item of recommendList" :key="item.id">
        <div class="item-img-wrapper">
	  		  <img class="item-img" :src="item.imgUrl"></img>
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
	data () {
		return {
			recommendList: [{
				id: '0001',
				imgUrl: 'http://imgs.qunarzz.com/p/p70/1809/e7/4941057a6aae702.jpg_256x160_9fee6ccb.jpg',
				title: '广州-丽江',
				desc: '含往返飞机票+4晚住宿'
			}, {
				id: '0002',
				imgUrl: 'http://imgs.qunarzz.com/p/p67/1512/a2/0ebfcd965b9391f7.jpg_256x160_04d5813d.jpg',
				title: '广州-三亚',
				desc: '含往返飞机票(含税)+4晚住宿'
			}, {
				id: '0003',
				imgUrl: 'https://imgs.qunarzz.com/p/p14/201302/28/218ac6605f1d637f93835fbb.jpg_256x160_bfee6c2d.jpg',
				title: '广州-桂林',
				desc: '含往返飞机票(含税)+9晚住宿'
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
  .item-img-wrapper
    overflow: hidden
    height: 0
    padding-bottom: 33.9%
    // padding-bottom: 62.5%
    .item-img
      width: 100%
  .item-info
  	padding: .1rem
  	.item-title
  		line-height: .54rem
  		font-size: .32rem
  		ellipsis()
  	.item-desc
  		line-height: .4rem
  		color: #ccc
  		ellipsis()
</style>