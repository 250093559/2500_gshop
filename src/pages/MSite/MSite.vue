<template>
	<div class="msite">
		<!--首页头部-->
		<HeaderTop :title="title">
			<span class="header_search" slot="left">
				<i class="iconfont icon-icon_search"></i>
			</span>
			<span class="header_login" slot="right">
				<span class="header_login_text">登陆 | 注册</span>
			</span>
		</HeaderTop>
		<!--首页导航-->
		<div class="msite_nav">
			<div class="swiper-container">
				<div class="swiper-wrapper">
					<div class="swiper-slide">
						<a href="javascript:;" class="link_to_food">
							<div class="food_container">
								<img src="./images/nav/1.jpg">
							</div>
							<span>甜品饮品</span>
						</a>
						
						<a href="javascript:;" class="link_to_food">
							<div class="food_container">
								<img src="./images/nav/2.jpg">
							</div>
							<span>商超便利</span>
						</a>
						
						<a href="javascript:;" class="link_to_food">
							<div class="food_container">
								<img src="./images/nav/3.jpg">
							</div>
							<span>美食</span>
						</a>
						
						<a href="javascript:;" class="link_to_food">
							<div class="food_container">
								<img src="./images/nav/4.jpg">
							</div>
							<span>简餐</span>
						</a>
						
						<a href="javascript:;" class="link_to_food">
							<div class="food_container">
								<img src="./images/nav/5.jpg">
							</div>
							<span>新店特惠</span>
						</a>
						
						<a href="javascript:;" class="link_to_food">
							<div class="food_container">
								<img src="./images/nav/6.jpg">
							</div>
							<span>准时达</span>
						</a>
						
						<a href="javascript:;" class="link_to_food">
							<div class="food_container">
								<img src="./images/nav/7.jpg">
							</div>
							<span>预订早餐</span>
						</a>
						
						<a href="javascript:;" class="link_to_food">
							<div class="food_container">
								<img src="./images/nav/8.jpg">
							</div>
							<span>土豪推荐</span>
						</a>
					</div>
					
					<div class="swiper-slide">
						<a href="javascript:;" class="link_to_food">
							<div class="food_container">
								<img src="./images/nav/1.jpg">
							</div>
							<span>甜品饮品</span>
						</a>
						
						<a href="javascript:;" class="link_to_food">
							<div class="food_container">
								<img src="./images/nav/2.jpg">
							</div>
							<span>商超便利</span>
						</a>
						
						<a href="javascript:;" class="link_to_food">
							<div class="food_container">
								<img src="./images/nav/3.jpg">
							</div>
							<span>美食</span>
						</a>
						
						<a href="javascript:;" class="link_to_food">
							<div class="food_container">
								<img src="./images/nav/4.jpg">
							</div>
							<span>简餐</span>
						</a>
						
						<a href="javascript:;" class="link_to_food">
							<div class="food_container">
								<img src="./images/nav/5.jpg">
							</div>
							<span>新店特惠</span>
						</a>
						
						<a href="javascript:;" class="link_to_food">
							<div class="food_container">
								<img src="./images/nav/6.jpg">
							</div>
							<span>准时达</span>
						</a>
						
						<a href="javascript:;" class="link_to_food">
							<div class="food_container">
								<img src="./images/nav/7.jpg">
							</div>
							<span>预订早餐</span>
						</a>
						
						<a href="javascript:;" class="link_to_food">
							<div class="food_container">
								<img src="./images/nav/8.jpg">
							</div>
							<span>土豪推荐</span>
						</a>
					</div>
				</div>
				
				<!--Add Pagination-->
			    <div class="swiper-pagination"></div>
			</div>
		</div>
		
		<!--首页附近商家-->
		<div class="msite_shop_list">
			<div class="shop_header">
				<i class="iconfont icon-option"></i>
				<span class="shop_header_title">附近商家</span>
			</div>
			<ShopList></ShopList>
		</div>
	</div>
</template>

<script>
import HeaderTop from '@/components/HeaderTop/HeaderTop'
import ShopList from '@/components/ShopList/ShopList'
import Swiper from 'swiper'   //swiper插件只引入这个和下面那个CSS就可以用了
import 'swiper/dist/css/swiper.min.css'
export default{
	data(){
		return {
			title:'佛山市禅城区港口路碧桂园城市花园'
		}
	},
	components:{
		HeaderTop,
		ShopList
	},
	mounted(){
		//创建一个Swiper实例对象，来实现轮播 教程详细https://www.swiper.com.cn/usage/index.html
		new Swiper ('.swiper-container', {
            loop: true,   //循环轮播
            // 如果需要分页器
            pagination: {
                el: '.swiper-pagination',
            }
        })
	}
}
</script>

<style lang="stylus" rel="stylesheet/stylus">
@import "../../common/stylus/mixins.styl"
.msite 
   width 100%
   .msite_nav
        bottom-border-1px(#e4e4e4)
        margin-top 45px
        height 200px
        background #fff
        .swiper-container
            width 100%
            height 100%
            .swiper-wrapper
                width 100%
                height 100%
                .swiper-slide
                    display flex
                    justify-content center
                    align-items center
                    flex-wrap wrap
                    width 100%
                    height 100%
                    .link_to_food
                        width 25%
                        .food_container
                            display block
                            width 100%
                            text-align center
                            padding-bottom 10px
                            img
                               display inline-block
                               width 50px
                               height 50px
                        span
                            display block
                            width 100%
                            text-align center
                            font-size 13px
                            color #666
                            padding-bottom 20px;  /*修改swiper对称问题*/
            .swiper-pagination
                >span.swiper-pagination-bullet-active
                    background #02a774        
   .msite_shop_list
       bottom-border-1px(#e4e4e4)
       margin-top 10px
       background #fff
       .shop_header
            padding 10px 10px 0
            .icon-option
                margin-left 5px
                color #999
            .shop_header_title
                color #999
                font-size 16px
                line-height 20px
       
</style>