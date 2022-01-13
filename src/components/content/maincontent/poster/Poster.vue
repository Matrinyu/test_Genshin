<template>
	<div>
		<div class="limit-mask">
			<div class="bg-mask"></div>
		</div>
		<div class="openvideo">
			<video class="cilck-video"
			controls="controls" width="895px" height="504px">
				<source src="../../../../assets/video/官网点击视频.mp4" type="video/mp4"></source>
			</video>
		</div>
		<div class="poster">
			<div class="bgWrap">
				<video id="bg" loop="loop" muted="muted" autoplay >
					<source src="../../../../assets/video/原神官网视频.mp4" type="video/mp4"></source>
				</video>
			</div>
			<div class="limit">
				<img src="../../../../assets/img/12.png" >
			</div>
			<div class="posterenter">
				<div class="video_enter">
					<div class="video_enter_icon"></div>
				</div>
			</div>
			<div class="ysdownload">
				<div class="QR -code">
					<div class="code"><img src="../../../../assets/img/官方二维码.png" ></div>
					<div class="code-icon"><img src="../../../../assets/img/二维码中间.jpg" ></div>
				</div>
				<div class="ps4-appstore">
					<div class="ps"></div>
					<div class="appstore"></div>
				</div>
				<div class="taptap-andriod">
					<div class="tap"></div>
					<div class="andriod"></div>
				</div>
				<div class="pc">
					<div class="pcpc"><img src="../../../../assets/img/pc.png" ></div>
				</div>
			</div>
			<div class="limitposter">
				<img class="lposter" 
				src="../../../../assets/img/poster/limit.jpg">
				<img class="close-icon"
				src="../../../../assets/img/poster/close.png">
			</div>
		</div>
	</div>
</template>

<script>
	export default {
		name: 'Poster',
	}
	
	window.addEventListener('load', function() {
		let bg = document.querySelector('#bg')
		let po = document.querySelector('.poster')
		let ysdl = document.querySelector('.ysdownload')
		let py = document.querySelector('.posterenter')
		let limit = document.querySelector('.limit')
		let limitposter = document.querySelector('.limitposter')
		let lposter = document.querySelector('.lposter')
		let close = document.querySelector('.close-icon')
		let mask = document.querySelector('.limit-mask')
		let clickopen = document.querySelector('.video_enter_icon')
		let openv = document.querySelector('.openvideo')
		let cv = document.querySelector('.cilck-video')
		//获取浏览器窗口高度和宽度
		let bh = document.documentElement.clientHeight
		let bw = document.documentElement.clientWidth
		//设置video高度
		bg.style.height = bh + 'px'
		po.style.height = bh + 'px'
		//设置下载栏位置
		let dlw = ysdl.offsetWidth
		ysdl.style.left = ( bw - dlw ) / 2  + 'px'
		//设置videoentry的位置
		let pyw = py.offsetWidth
		py.style.left = ( bw - pyw ) / 2  + 'px'
		//设置limit图位置
		let lmtpw = limitposter.offsetWidth
		let lmtph = limitposter.offsetHeight
		lposter.style.left = ( bw - lmtpw) / 2 + 'px'
		lposter.style.top = ( bh - lmtph) / 2 + 'px'
		close.style.right = ( bw - lmtpw) / 2 - 57 + 'px'
		close.style.top = ( bh - lmtph) / 2 + 'px'
		//设置video位置
		openv.style.left = ( bw - 896) / 2 + 'px'
		//控制limit图是否显示
		limit.addEventListener('click', function() {
			lposter.style.display = 'block'
			mask.style.display = 'block'
			close.style.display = 'block'
		})
		//limit关闭键
		close.addEventListener('click', function() {
			lposter.style.display = 'none'
			mask.style.display = 'none'
			close.style.display = 'none'
		})
		//蒙板
		mask.addEventListener('click', function() {
			lposter.style.display = 'none'
			mask.style.display = 'none'
			close.style.display = 'none'
			openv.style.display = 'none'
			cv.currentTime = 0
			cv.pause()
		})
		//控制视频是否播放
		clickopen.addEventListener('click', function() {
			mask.style.display = 'block'
			openv.style.display = 'block'
			cv.play()
		})
	})
		
</script>

<style>
.limit-mask{
	position: fixed;
	box-sizing: border-box;
	left: 0;
	top: 0;
	width: 100%;
	height: 100vh;
	background: rgba(0, 0, 0, 0.4);
	z-index: 99;
	opacity: 1;
	display: none;
}
.bg-mask{
	width: 100%;
	min-height: 100%;
	height: auto;
}
.poster{
	position: relative;
	width: auto;
}
#bg{
	object-fit: fill;
	width: 100%;
}
.limit{
	position: absolute;
	left: 20px;
	bottom: 20px;
}
.limit img{
	width: 100px;
	cursor: pointer;
}
.limitposter{
	width: 854px;
	height: 642px;
}
.lposter{
	display: none;
	width: 854px;
	height: 642px;
	position: fixed;
	z-index: 100;
}
.close-icon{
	display: none;
	width: 57px;
	height: 57px;
	position: fixed;
	cursor: pointer;
	z-index: 101;
}
.posterenter{
	position: absolute;
	bottom: 200px;
	background-image: url(../../../../assets/img/中间播放功能.png);
	background-repeat: no-repeat;
	width: 356px;
	height: 76px;
}
.video_enter{
	position: relative;
	width: 50px;
	height: 50px;
	border-radius: 50%;
	margin: auto;
	cursor: pointer;
	transform: translateY(13px);
	background-color: #ffffff;
	opacity: 1;
}
.video_enter:hover{
	opacity: 0.1;
}
.video_enter_icon{
	background-image: url(../../../../assets/img/播放图标.png);
	background-repeat: no-repeat;
	position: absolute;
	left: 11px;
	top: 11px;
	width: 30px;
	height: 30px;
	opacity: 1;
}
.openvideo{
	display: none;
	position: fixed;
	top: 250px;
	z-index: 101;
}
.ysdownload{
	position: absolute;
	bottom: 50px;
	height: 120px;
	cursor: pointer;
}
.QR{
	display: inline-block;
	position: relative;
	width: 100px;
	vertical-align: top;
	margin-top: 5px;
	padding-right: 10px;
}
.code img{
	width: 100px;
	height: 100px;
}
.code-icon{
	display: inline-block;
	position: absolute;
	top: 37.5px;
	left: 37.5px;
}
.code-icon img{
	width: 25px;
	height: 25px;
	border: 3px solid #4c5e7e;
}
.ps4-appstore{
	display: inline-block;
	width: 155px;
	vertical-align: top;
	padding-right: 10px;
}
.ps{
	background-image: url(../../../../assets/img/ps4.png);
	background-repeat: no-repeat;
	width: 160px;
	height: 55px;
}
.appstore{
	background-image: url(../../../../assets/img/TapTap下载.png);
	background-repeat: no-repeat;
	width: 160px;
	height: 55px;
}
.taptap-andriod{
	display: inline-block;
	width: 155px;
	vertical-align: top;
	padding-right: 10px;
}
.tap{
	background-image: url(../../../../assets/img/TapTap下载.png);
	background-repeat: no-repeat;
	width: 160px;
	height: 55px;	
}
.andriod{
	background-image: url(../../../../assets/img/安卓下载.png);
	background-repeat: no-repeat;
	width: 160px;
	height: 55px;	
}
.pc{
	display: inline-block;
	vertical-align: top;
	padding-right: 10px;
}
.pcpc{
	height: 100px;
	width: 100px;
}
</style>
