<template lang="html">
    <article class="">
    	<!-- 轮播图 -->
    	    <Slider :items="items" :cname="$style.slider"/>
		<!-- 5个小圆导航入口 -->		
		<section :class="$style.list">
			<div :class="$style.item" v-for="item in enters">
				<router-link :to={name:item.href}>
					<img :src="item.img" alt="item.title">
					<h4>优惠券</h4>
				</router-link>
			</div>
		</section>
    </article>
</template>

<script>
import Slider from '../core/slider.vue'
export default {
    data() {
        return {
        	//轮播图数组
            items:[
            	{
            		href:'',
            		src:'//img12.360buyimg.com/jrpmobile/jfs/t15841/116/2678213635/24286/b0e919db/5ab386c2Ndc61eee8.jpg'
            	},
            	{
            		href:'',
            		src: 'https://img12.360buyimg.com/jrpmobile/jfs/t14677/259/2692320740/48815/dc123010/5ab386a9N6d74c344.jpg'
            	}
            ],
            enters:[
            	{
            		title:'优惠券',
            		href:'',
            		img:'//img12.360buyimg.com/jrpmobile/jfs/t3991/64/2521945388/12110/93c0139/58d1e462Ncf294123.png?width=132&height=132'
            	},
            	{
            		title:'优惠券',
            		href:'',
            		img:'//img12.360buyimg.com/jrpmobile/jfs/t3991/64/2521945388/12110/93c0139/58d1e462Ncf294123.png?width=132&height=132'
            	},
            	{
            		title:'优惠券',
            		href:'',
            		img:'//img12.360buyimg.com/jrpmobile/jfs/t3991/64/2521945388/12110/93c0139/58d1e462Ncf294123.png?width=132&height=132'
            	},
            	{
            		title:'优惠券',
            		href:'',
            		img:'//img12.360buyimg.com/jrpmobile/jfs/t3991/64/2521945388/12110/93c0139/58d1e462Ncf294123.png?width=132&height=132'
            	},
            	{
            		title:'优惠券',
            		href:'',
            		img:'//img12.360buyimg.com/jrpmobile/jfs/t3991/64/2521945388/12110/93c0139/58d1e462Ncf294123.png?width=132&height=132'
            	}
            ]
        }
    },
    components:{


    	Slider,
    }
}
</script>

<style lang="scss" module>
@import '../../css/element.scss';
article{
	margin-top: 120px;
	.slider img{
		width: 100%;
	}
	.list{
		@include list(row);//继承element.css里的样式
		padding:40px 0 20px 0;
		justify-content:space-around;//两端对齐---5个均分
		a {
			text-decoration: none;
		}
		.item{
			text-align: center;
			img{
				display: inline-block;
				width: 90px;
			}
			h4{
				font-size: 26px;
				margin-top: 12px;
				color: #666;
			}
		}
	}
}
</style>
