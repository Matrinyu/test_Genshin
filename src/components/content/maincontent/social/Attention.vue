<template>
	<div class="attent-wrap">
		<div class="attent-container">
			<div class="attent-close">
				<div class="arrowhead"></div>
			</div>
			<ul>
				<li class="attent-wx">
					<p>关注我们</p>
					<p><img src="../../../../assets/img/social/关注wx.png"></p>
					<p>扫码关注微信</p>
				</li>
				<li class="lii">
					<a href="javascript:;">
						<span></span>
						官方微博
					</a>
				</li>
				<li class="lii">
					<a href="javascript:;">
						<span></span>
						&nbsp;TapTap
					</a>
				</li>
				<li class="lii">
					<a href="javascript:;">
						<span></span>
						官方社区
					</a>
				</li>
			</ul>
		</div>
	</div>
</template>

<script>
	export default {
		name: 'Attention',
		mounted() {
			window.addEventListener('scroll', this.windowScroll)
		},
		methods: {
			windowScroll() {
				if(document.documentElement.scrollTop > 800){
					document.querySelector('.attent-wrap').style.visibility = 'visible'
				}else{
					document.querySelector('.attent-wrap').style.visibility = 'hidden'
				}
			}
		}
	}
	
	window.addEventListener('load', function() {
		let attwp = document.querySelector('.attent-wrap')
		let attclose = document.querySelector('.attent-close')
		let arrow = document.querySelector('.arrowhead')
		
		let flag = 0
		attclose.addEventListener('click', function() {
			if(flag === 0){
				attwp.style.right = - 180 + 'px'
				arrow.className = 'arrowheadclick' 
				flag = 1
			}else{
				attwp.style.right = 0
				arrow.className = 'arrowhead'
				flag = 0
			}
		})
	})
</script>

<style>
.attent-wrap{
	z-index: 10;
	visibility: hidden;
	position: fixed;
	top: 30%;
	right: 0;
	font-size: 18px;
	width: 180px;
	height: auto;
	background-color: #f7f7f7;
	transition: ease 0.7s;
}
.attent-container{
	position: relative;
}
.attent-close{
	position: absolute;
	top: 0;
	left: -30px;
	width: 30px;
	height: 50px;
	border-top-left-radius: 5px;
	border-bottom-left-radius: 5px;
	background-color: #333;
	display: flex;
	justify-content: center;
	align-items: center;
	cursor: pointer;
}
.arrowhead{
	background: url(../../../../assets/img/social/箭头.png) no-repeat;
	width: 20px;
	height: 20px;
	transition: ease .8s;
}
.arrowheadclick{
	background: url(../../../../assets/img/social/箭头.png) no-repeat;
	width: 20px;
	height: 20px;
	transition: ease .8s;
	transform: rotateY(180deg);
}
.attent-wx p{
	position: ;
	display: flex;
	justify-content: center;
	margin-bottom: 10px;
}
.attent-wx p:nth-child(1){
	margin-top: 20px;
}
.attent-wx img{
	width: 147px;
	height: 147px;
}
li a{
	text-decoration: none;
	display: flex;
	align-items: center;
	justify-content: center;
	color: #464646;
	width: 180;
	height: 45px;
}
li:nth-child(2) span{
	background-image: url(../../../../assets/img/social/微博.png);
	background-repeat: no-repeat;
	width: 30px;
	height: 30px;
	display: inline-block;
	margin-right: 20px;
}
li:nth-child(2):hover span{
	background-image: url(../../../../assets/img/social/微博h.png);
	background-repeat: no-repeat;
	width: 30px;
	height: 30px;
	display: inline-block;
	margin-right: 20px;
}
li:nth-child(3) span{
	background-image: url(../../../../assets/img/social/taptap.png);
	background-repeat: no-repeat;
	width: 30px;
	height: 30px;
	display: inline-block;
	margin-left: -5px;
	margin-right: 20px;
}
li:nth-child(3):hover span{
	background-image: url(../../../../assets/img/social/taptaph.png);
	background-repeat: no-repeat;
	width: 30px;
	height: 30px;
	display: inline-block;
	margin-right: 20px;
}
li:nth-child(4) span{
	background-image: url(../../../../assets/img/social/米游社h.png);
	background-repeat: no-repeat;
	width: 20px;
	height: 20px;
	background-size: cover;
	display: inline-block;
	margin-right: 20px;
}
li:nth-child(4):hover span{
	background-image: url(../../../../assets/img/social/米游社h.png);
	background-repeat: no-repeat;
	width: 20px;
	height: 20px;
	display: inline-block;
	margin-right: 20px;
}
.lii:nth-child(n+2):hover{
	background-color: #464646;

}
.lii:nth-child(n+1):hover a{
	color: #1296db;	
}
</style>
