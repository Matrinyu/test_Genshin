<template>
	<div class="foot-wrap">
		<div class="foot-logo">
			<img class="logo-one" src="../../../../assets/img/foot/mhylogo.png" >
			<span class="logo-zero">|</span>
			<img class="logo-two" src="../../../../assets/img/foot/yuanslogo.png" >
		</div>
		<div class="foot-info">
			<div class="foot-link">
				<div class="link-item">
					<a href="javascript:;">用户协议</a>
					|
					<a href="javascript:;">隐私政策</a>
					|
					<a href="javascript:;">自律公约</a>
					|
					<a href="javascript:;">家长监护工程</a>
					|
					<a href="javascript:;">关于我们</a>
					|
					<a href="javascript:;">联系我们</a>
					|
					<a href="javascript:;">加入我们</a>
				</div>
			</div>
			<div class="font">
				<span>健康游戏忠告：抵制不良游戏，拒绝盗版游戏。注意自我保护，谨防受骗上当。适度游戏益脑，沉迷游戏伤身。合理安排时间，享受健康生活。</span>
			</div>
			<div class="font">
				<span>沪公网安备31010402001113号  |  增值电信业务经营许可证：沪B2-20190555</span>
			</div>
			<div class="font">
				<span>沪ICP备19018275号-4 | 沪网文〔2019〕3168-216号 | 国新出审【2019】2978号</span>
			</div>
			<div class="font">
				<span>互联网违法不良信息举报邮箱: tousu@mihoyo.com 互联网违法不良信息举报电话: 021-60371750 (工作时间：每天10点 - 20点）</span>
			</div>
			<div class="font">
				<span>亲爱的市民朋友，上海警方反诈劝阻电话“962110”系专门针对避免您财产被骗受损而设，请您一旦收到来电，立即接听</span>
			</div>
			<div class="font">
				<span>未成年成长关爱热线：021-60371740</span>
			</div>
			<div class="font">
				<span>© 2020 米哈游版权所有 | 上海米哈游影铁科技有限公司 客服电话：400-666-6312</span>
			</div>
			<div class="foot-img">
				<a href="javascript:;"></a>
				<a href="javascript:;"></a>
				<a href="javascript:;"></a>
				<a href="javascript:;"></a>
				<a href="javascript:;"></a>
				<a href="javascript:;"></a>
			</div>
		</div>
	</div>
</template>

<script>
	export default {
		name: 'Foot',
	}
</script>

<style>
.foot-wrap{
	width: 100%;
	height: 350px;
	background-color: #000000;
	display: flex;
	justify-content: center;
	align-items: center;
}
.foot-logo{
	display: flex;
	align-items: center;
	width: 300px;
	height: 300px;
}
.foot-info{
	width: 900px;
	height: 300px;
	margin-left: 60px;
	color: #aaa;
}
.logo-one{
	width: 119px;
	height: 42px;
}
.logo-zero{
	margin: 20px;
	width: 1px;
	height: 30px;
	background: #666;
}
.logo-two{
	width: 110px;
	height: 70px;
}
.foot-link{
	width: 100%;
	height: 50px;
}
.foot-wrap{
	font-size: 14px;
}
.foot-link a{
	text-decoration: none;
	color: #ffffff;
	margin: 5px;
}
.font{
	margin-top: 4px;
}
.foot-img{
	display: flex;
	width: 100%;
	height: auto;
	justify-content: flex-start;
	margin-top: 10px;
}
.foot-img a{
	margin-right: 15px;
	margin-bottom: 10px;
	width: 116px;
	height: 46px;
	background-size: 116px 46px;
}
.foot-img a:nth-child(1){
	background-image: url(../../../../assets/img/foot/认证.png);
	background-repeat: no-repeat;
}
.foot-img a:nth-child(2){
	background-image: url(../../../../assets/img/foot/举报.png);
	background-repeat: no-repeat;
}
.foot-img a:nth-child(3){
	background-image: url(../../../../assets/img/foot/有害举报.png);
	background-repeat: no-repeat;
}
.foot-img a:nth-child(4){
	background-image: url(../../../../assets/img/foot/单位.png);
	background-repeat: no-repeat;
}
.foot-img a:nth-child(5){
	background-image: url(../../../../assets/img/foot/phone.png);
	background-repeat: no-repeat;
}
.foot-img a:nth-child(6){
	background-image: url(../../../../assets/img/foot/lisence.png);
	background-repeat: no-repeat;
}
</style>
