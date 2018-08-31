<template>
	<div class="footer_guide">
		<span class="guide_item" :class="{on:'/msite' === $route.path}" @click="goTo('/msite')">
			<span class="item_icon">
				<i class="iconfont icon-home"></i>
			</span>
			<span>外卖</span>
		</span>
		
		<span class="guide_item" :class="{on:'/search' === $route.path}" @click="goTo('/search')">
			<span class="item_icon">
				<i class="iconfont icon-icon_search"></i>
			</span>
			<span>搜索</span>
		</span>
		
		<span class="guide_item" :class="{on:'/order' === $route.path}" @click="goTo('/order')">
			<span class="item_icon">
				<i class="iconfont icon-danju"></i>
			</span>
			<span>订单</span>
		</span>
		
		<span class="guide_item" :class="{on:'/profile' === $route.path}" @click="goTo('/profile')">
			<span class="item_icon">
				<i class="iconfont icon-gerenxinxi"></i>
			</span>
			<span>我的</span>
		</span>
	</div>
</template>

<script>
export default{
	methods:{
	   goTo(path){
	   	  this.$router.replace(path);  //这个方法不会向history里面添加新的记录,push会产生记录
	   },
	   isCurrent(path){
	   	  return this.$route.path===path;
	   }
	}
}
</script>
<style lang="stylus" rel="stylesheet/stylus">
@import "../../common/stylus/mixins.styl"
.footer_guide
    top-border-1px(#e4e4e4)
    position fixed
    z-index 100
    left 0
    right 0
    bottom 0
    background-color #fff
    width 100%
    height 50px
    display flex   /*弹性布局*/
    .guide_item
       display flex
       flex 1         /*按比分宽*/
       text-align center
       flex-direction column  /*垂直显示   row水平显示   column-reverse垂直顺序相反    row-reverse水平顺序相反*/
       align-items center     /*水平垂直居中对齐*/
       margin 5px
       color #999999
       &.on
          color #02a774
       span
         font-size 12px
         margin-top 2px
         margin-bottom 2px
         .iconfont
            font-size 22px         
</style>