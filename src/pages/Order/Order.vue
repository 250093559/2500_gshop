<template>
	<div class="order">
		<HeaderTop :title="title"></HeaderTop>
		<section class="order_no_login">
			<img src="./images/person.png">
			<h3>登陆后查看外卖订单</h3>
			<button>立即登陆</button>
		</section>
	</div>
</template>

<script>
import HeaderTop from '@/components/HeaderTop/HeaderTop'
export default{
	data(){
		return {
			title:'订单列表'
		}
	},
	components:{
		HeaderTop
	}
}
</script>

<style lang="stylus" rel="stylesheet/stylus">
@import "../../common/stylus/mixins.styl"
.order
   width 100%
   .header /*头部公共css*/
        background-color #02a774
        position fixed
        z-index 100
        left 0
        top 0
        width 100%
        height 45px
        .header_title
            position absolute
            top 50%
            left 50%
            transform translate(-50%, -50%)
            width 30%
            color #fff
            font-size 22px
            text-align center
            .header_title_text
                font-size 20px
                color #fff
                display block
   .order_no_login
        padding-top 140px
        width 60%
        margin 0 auto
        text-align center
        >img
            display block
            width 100%
            height 30%
        >h3
            padding 10px 0
            font-size 17px
            color #6a6a6a
        >button
            display inline-block
            background #02a774
            font-size 14px
            color #fff
            border 0
            outline none
            border-radius 5px
            padding 10px 20px

</style>