<template>
	<div class="head-nav">
		<audio class="bmg" 
		src="../../../assets/radio/原神官网视频.mp3" 
		autoplay="autoplay" loop="loop" >
			当前浏览器不支持audio
		</audio>
		<div class="head-left">
			<div class="head-music">
				<img class="icon-music" src="../../../assets/img/播放开.png" >
				<img class="music-icon" src="../../../assets/img/播放关.png">
			</div>
			<div class="head-logo"></div>
		</div>
		<div class="head-center">
			<a href="javascript:;">首&nbsp页</a>
			<a href="javascript:;">新&nbsp闻</a>
			<a href="javascript:;">角&nbsp色</a>
			<a href="javascript:;">世&nbsp界</a>
			<a href="javascript:;">漫&nbsp画</a>
			<a href="javascript:;">社&nbsp区</a>
		</div>
		<div class="head-right">
			<div class="head-logintext">登&nbsp录</div>
			<div class="head-loginicon">
				<img src="../../../assets/img/登录.png" >
			</div> 
		</div>
		<div class="mhy-account">
			<div class="account-logo">
				<img src="../../../assets/img/account/mhy.png" >
				</div>
			<div class="account-login">
				<div class="close-account">
					<img src="../../../assets/img/account/关闭.png" >
				</div>
				<div class="login-type">
					<div class="alltypes">
						<div class="account-item typeone"><span>验证码登录</span></div>
						<div class="account-item typetwo"><span>密码登录</span></div>
					</div>
				</div>
				<div class="form-select">
					<div class="form-show">
						<div class="form-1">
							<form>
								<div class="tel">
									<div class="tel-container">
										<input type="tel" placeholder="手机号登录/注册"
										style="width:368px;height: 46px;border: none;"/>
									</div>
								</div>
								<div class="ident">
									<div class="ident-container">
										<input type="tel" placeholder="验证码"
										style="width:248px;height: 46px;border: none;"/>
										<div class="getident" style="width: 120px;">获取验证码</div>
									</div>
								</div>
							</form>
						</div>
						<div class="form-2">
							<form>
								<div class="tel">
									<div class="tel-container">
										<input type="tel" placeholder="手机号/邮箱"
										style="width:368px;height: 46px;border: none;"/>
									</div>
								</div>
								<div class="ident">
									<div class="ident-container">
										<input type="tel" placeholder="密码"
										style="width:368px;height: 46px;border: none;"/>
									</div>
								</div>
							</form>
						</div>
					</div>
				</div>
				<div class="mhy-login">
					<div class="login-item"><span>登&nbsp;录</span></div>
				</div>
				<div class="register-container">
					<div class="register">
						<a href="javascript:;">登录遇到问题？</a>
						<a href="javascript:;">立即注册</a>
					</div>
				</div>
				<div class="login-tips-container">
					<div class="login-tips">
						<span>未注册的手机验证后将自动登录。注册/登录即代表您同意并遵守</span>
						<a href="javascript:;">《米哈游通行证用户服务协议</a>
						<a href="javascript:;">《米哈游通行证用户个人信息及隐私保护政策</a>
					</div>
				</div>
			</div>
		</div>
	</div>
	</nav-bar>
</template>

<script>
	export default {
		name: 'HeadBar',
		methods:{
			
		}
	}
	
	window.addEventListener('load', function() {
		let hmusic = document.querySelector('.head-music')
		let bgm = document.querySelector('.bmg')
		let bgmmusic = document.querySelector('.music-icon')
		let musicbgm = document.querySelector('.icon-music')
		let mhyaccount = document.querySelector('.mhy-account')
		let tone = document.querySelector('.typeone')
		let ttwo = document.querySelector('.typetwo')
		let fmshow = document.querySelector('.form-show')
		let login = document.querySelector('.head-logintext')
		let atclose = document.querySelector('.close-account')
		
		var flag
		hmusic.addEventListener('click', function() {
			console.log(flag)
			if(flag == true || flag == undefined){
				musicbgm.style.display = 'block'
				bgmmusic.style.display = 'none'
				bgm.play()
				flag = false
			}else{
				musicbgm.style.display = 'none'
				bgmmusic.style.display = 'block'
				bgm.pause()
				flag = true
			}
		})
		
		let bw = document.documentElement.clientWidth
		mhyaccount.style.left = ( bw - 450 ) / 2 + 'px'
		
		login.addEventListener('click', function() {
			mhyaccount.style.display = 'block'
		})
		atclose.addEventListener('click', function() {
			mhyaccount.style.display = 'none'
		})
		
		tone.addEventListener('click', function() {
			fmshow.className = 'form-show'
		})
		ttwo.addEventListener('click', function() {
			fmshow.className = 'form-show-change'
		})
	})
</script>

<style>
.head-nav{
	position: fixed;
	top: 0;
	left: 0;
	width: 100%;
	height: 66px;
	background-color: #181818;
	opacity: 0.9;
	z-index: 11;
}
.mhy-account{
	position: absolute;
	top: 266px;
	right: 400px;
	width: 450px;
	height: 525px;
	font-size: 18px;
	display: none;
}
.account-logo{
	width: 100%;
	height: 40px;
	display: flex;
	justify-content: center;
}
.account-logo img{
	width: 107px;
	height: 38px;
	display: inline-block;
}
.account-login{
	width: 100%;
	height: 475px;
	background-color: #fff;
	margin-top: 10px;
	border-radius: 5px;
}
.close-account{
	width: 100%;
	height: 40px;
	position: relative;
}
.close-account img{
	width: 18px;
	height: 18px;
	position: absolute;
	top: 15px;
	right: 20px;
	cursor: pointer;
}
.login-type{
	width: 100%;
	height: 48px;
	display: flex;
	justify-content: center;
}
.alltypes{
	width: 400px;
	height: 48px;
	border-bottom: 1px solid #c1c1c1;
	display: flex;
	justify-content: center;
}
.account-item{
	width: 185px;
	height: 47px;
	color: #6a6a6a;
	box-sizing: border-box;
	text-align: center;
	padding-top: 7px;
	cursor: pointer;
}
.typeone:hover, .typetwo:hover{
	border-bottom: 3px solid #757575;
}
.form-select{
	width: 450px;
	overflow: hidden;
}
.form-show{
	width: 900px;
	display: flex;
	flex: 1;
	transform: translateX(0px);
}
.form-show-change{
	width: 900px;
	display: flex;
	flex: 1;
	transform: translateX(-450px);
}
.form-1, .form-2{
	width: 450px;
	display: flex;
	justify-content: center;
}
.tel, .ident{
	width: 100%;
	height: 60px;
	box-sizing: border-box;
	display: flex;
	justify-content: center;
	margin-top: 20px;
}
.tel{
	padding-top: 10px;
}
.tel-container, .ident-container{
	width: 370px;
	height: 48px;
	display: flex;
	justify-content: center;
	align-items: center;
	border: 1px solid #aaaaaa;
	border-radius: 5px;
}
.mhy-login{
	width: 100%;
	height: 48px;
	margin-top: 10px;
	display: flex;
	justify-content: center;
}
.login-item{
	width: 370px;
	height: 48px;
	border-radius: 3px;
	color: #ffffff;
	background-color: #3b4354;	
	display: flex;
	justify-content: center;
	align-items: center;
	cursor: pointer;
}
.getident{
	padding-left: 10px;
	border-left: 1px solid #bebebe;
	font-size: 16px;
	color: #717171;
}
.register-container{
	width: 100%;
	height: 20px;
	display: flex;
	justify-content: center;
	margin-top: 15px;
}
.register{
	width: 370px;
	height: 20px;
	display: flex;
	justify-content: space-between;
}
.register a{
	text-decoration: none;
	color: #9e9e9e;
}
.login-tips-container{
	width: 100%;
	margin-top: 20px;
	display: flex;
	justify-content: center;
	font-size: 16px;
}
.login-tips a{
	text-decoration: none;
	color: #868686;
}
.login-tips{
	width: 370px;
}
.head-left, .head-center, .head-right, .head-music, .head-logo,
.head-logintext, .head-loginicon{
	display: inline-block;
	vertical-align: top;
}
.head-left{
	position: relative;
	width: auto;
	height: 100%;
}
.head-center{
	position: relative;
	width: auto;
	height: 100%;
	box-sizing: content-box;
}
.head-right{
	position: relative;
	width: auto;
	height: 100%;
	margin-right: 45px;
	float: right;
}
.head-music{
	width: 30px;
	height: 30px;
	cursor: pointer;
	position: absolute;
	top: 18px;
	left: 70px;
}
.icon-music{
	display: none;
}
.head-music img{
	width: 30px;
	height: 30px;
	cursor: pointer;
}
.head-logo{
	background-image: url(../../../assets/img/原神主页logo.png);
	background-repeat: no-repeat;
	width: 317px;
	height: 100%;
	opacity: 1;
}
.head-center a{
	text-decoration: none;
	margin: 0 30px;
	color: #ccc;
	line-height: 60px;
	font-size: 17px;
	font-weight: normal;
	font-stretch: normal;
	letter-spacing: 0px;
	display: inline-block;
	border-top: 6px solid transparent;
}
.head-center a:hover{
	text-shadow: 0 0 10px #69e0ff, 0 0 20px #69e0ff, 0 0 40px #69e0ff;
	border-top: 6px solid #55ffff;
	color: #fff;
}
.head-logintext{
	font-size: 17px;
	color: #ccc;
	cursor: pointer;
	line-height: 66px;
	margin-right: 20px;
	opacity: 0.6;
}
.head-loginicon{
	width: 20px;
	height: 100%;
}
.head-loginicon img{
	position: absolute;
	top: 20px;
	width: 26px;
	height: 26px;
	opacity: 0.8;
}
.head-logintext:hover{
	opacity: 1;
}
</style>
