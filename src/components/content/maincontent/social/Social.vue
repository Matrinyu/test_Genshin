<template>
	<div class="social-share">
		<li class="weibo"></li>
		<li class="wechat"></li>
		<li class="qq"></li>
		<li class="share">
			<div class="share-allitems">
			</div>
		</li>
	</div>
</template>

<script>
	export default {
		name: 'Social',
	}
</script>

<style>
.social-share{
	width: 100%;
	height: 52px;
	background-color: #0f0f0f;
	border-bottom: #1a1a1a solid 2px;
	list-style-type: none;
	display: flex;
	line-height: 52px;
	justify-content: center;
	align-items: center;
}
.weibo, .wechat, .qq, .share{
	position: relative;
	width: 32px;
	height: 32px;
	line-height: 32px;
	margin-right: 34px;
	opacity: 0.4;
	cursor: pointer;
	background-size: contain;
}
.share{
	margin-right: 0;
	position: relative;
}
.weibo:hover, .wechat:hover, .qq:hover, .share:hover{
	opacity: 1;
}
.weibo{
	background-image: url(../../../../assets/img/social/新浪微博.png);
	background-repeat: no-repeat;
	width: 32px;
	height: 32px;
}
.wechat{
	background-image: url(../../../../assets/img/social/微信.png);
	background-repeat: no-repeat;
	width: 32px;
	height: 32px;
}
.qq{
	background-image: url(../../../../assets/img/social/qq.png);
	background-repeat: no-repeat;
	width: 32px;
	height: 32px;
}
.share{
	background-image: url(../../../../assets/img/social/分享方式.png);
	background-repeat: no-repeat;
	width: 32px;
	height: 32px;
}
</style>
