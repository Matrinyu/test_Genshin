<template>
	<div class="news">
		<h3>新&nbsp闻&nbsp资&nbsp讯</h3>
		<div class="news-content">
			<div class="news-swiper">
				<new-swiper></new-swiper>
			</div>
			<div class="news-context">
				<ul class="news-bar">
					<li class="news-bar-item">最新</li>
					<li class="news-bar-item">新闻</li>
					<li class="news-bar-item">公告</li>
					<li class="news-bar-item">活动</li>
				</ul>
				<div class="allnews">
					<ul></ul>
					<ul></ul>
					<ul></ul>
				</div>
			</div>
		</div>
	</div>
</template>

<script>
	import NewSwiper from './newssuiper/NewSwiper.vue'
	
	export default {
		name: 'News',
		components:{
			NewSwiper
		},
		methods:{
			
		}
	}

	window.addEventListener('load', function() {
		//获取浏览器窗口高度和宽度
		let bh = document.documentElement.clientHeight
		let bw = document.documentElement.clientWidth
		let nh = document.querySelector('.news')
		//news高度
		nh.style.height = bh - 66 + 'px'
	})
	
</script>

<style>
ul, li{
	list-style: none;
}
.news{
	display: flex;
  flex-direction: column;
	width: 100%;
	background-image: url(../../../../assets/img/蒙德酒馆.jpg);
	background-repeat: no-repeat;
	background-position: center;
	background-size: cover;
}
.news h3{
	position: relative;
	margin: 183px auto 60px;
	font-size: 50px;
	font-weight: 400;
	text-align: center;
	color: #fff;
}
.news h3::before{
	content: '';
	position: absolute;
	top: 50%;
	width: 385px;
	height: 14px;
	background-image: url(../../../../assets/img/news/newsbe.png);
	background-repeat: no-repeat;
	left: 0;
	transform: translate(calc(-100% - 32px), -50%);
}
.news h3::after{
	content: '';
	position: absolute;
	top: 50%;
	width: 385px;
	height: 14px;
	background-image: url(../../../../assets/img/news/newaf.png);
	background-repeat: no-repeat;
	right: 0;
	transform: translate(calc(100% + 32px), -50%) rotateY(180deg);
}
.news-content{
	display: flex;
	justify-content: center;
	height: 400px;
	margin: 0 auto;
}
.news-swiper{
	width: 640px;
}
.news-context{
	position: relative;
	width: 640px;
	margin: 0;
	background: rgba(38,18,12,0.62);
}
.news-bar{
	display: flex;
	align-items: flex-start;
	width: 592px;
	margin: 35px auto 0;
	border-bottom: 3px solid rgba(255,255,255,0.1);
}
.news-bar-item{
	position: relative;
	padding: 0 19px 12px;
	font-size: 18px;
	text-align: center;
	cursor: pointer;
	color: #FFF;
}

</style>
