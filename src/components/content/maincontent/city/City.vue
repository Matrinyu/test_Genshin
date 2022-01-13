<template>
	<div class="city">
		<ul class="citylist">
			<li class="citylist-item">
				<div class="item-bg"></div>
				<a href="javascript:;">
					<p>蒙德城</p>
				</a>
				<div class="itme-char"></div>
			</li>
			<li class="citylist-item">
				<div class="item-bg"></div>
				<a href="javascript:;">
					<p>璃月港</p>
				</a>
				<div class="itme-char"></div>
			</li>
			<li class="citylist-item">
				<div class="item-bg"></div>
				<a href="javascript:;">
					<p>稻妻城</p>
				</a>
				<div class="itme-char"></div>
			</li>
			<li class="citylist-item">
				<div class="item-bg"></div>
				<a href="javascript:;">
					<p>敬请期待</p>
				</a>
				<div class="itme-char"></div>
			</li>
		</ul>
	</div>
</template>

<script>
	export default {
		name: 'City',
	}

</script>

<style>
ul li{
	list-style: none;
}
.city{
	width: 100%;
}
.citylist{
	overflow: hidden;
}
.citylist-item{
	position: relative;
	width: 100%;
	height: 260px;
	background: center no-repeat;
	background-size: 100% auto;
	cursor: pointer;
	overflow: hidden;
}
.item-bg{
	position: absolute;
	top: 0;
	left: 0;
	display: block;
	width: 100%;
	height: 100%;
	background: contain no-repeat;
	background-size: 1920px 260px;
	transition: transform 0.4s 0s ease-out;
}
.citylist-item:nth-child(1) .item-bg{
	background-image: url(../../../../assets/img/city/蒙德.jpg);
	background-repeat: no-repeat;
}
.citylist-item:nth-child(2) .item-bg{
	background-image: url(../../../../assets/img/city/璃月.jpg);
	background-repeat: no-repeat;
}
.citylist-item:nth-child(3) .item-bg{
	background-image: url(../../../../assets/img/city/稻妻.jpg);
	background-repeat: no-repeat;
}
.citylist-item:nth-child(4) .item-bg{
	background-image: url(../../../../assets/img/city/黑.jpg);
	background-repeat: no-repeat;
}
.citylist-item:nth-child(1):hover .item-bg{
	background-image: url(../../../../assets/img/city/蒙德.jpg);
	background-repeat: no-repeat;
	transform: scale(1.05,1.05);
}
.citylist-item:nth-child(2):hover .item-bg{
	background-image: url(../../../../assets/img/city/璃月.jpg);
	background-repeat: no-repeat;
	transform: scale(1.05,1.05);
}
.citylist-item:nth-child(3):hover .item-bg{
	background-image: url(../../../../assets/img/city/稻妻.jpg);
	background-repeat: no-repeat;
	transform: scale(1.05,1.05);
}
.citylist-item a{
	text-decoration: none;
	display: inline-block;
	position: relative;
	z-index: 3;
	font-size: 36px;
	color: #fff;
	line-height: 260px;
	width: 100%;
	height: 260px;
	background: center no-repeat;
	background-size: 132px;
	text-align: center;
	text-shadow: 0 2px 6px rgb(0 0 0 / 20%);
	margin: 0;
	overflow: hidden;
}
.citylist-item:not(:last-child) .itme-char{
	position: absolute;
	z-index: 4;
	top: 0;
	right: 0;
	display: block;
	width: 100%;
	height: 260px;
	background-repeat: no-repeat;
	background-position: right;
	background-size: 960px 260px;
	opacity: 0;
	transition: all 0.2s 0s ease-in;
	border: #fff solid 6px;
	box-sizing: border-box;
}
.citylist-item .itme-char:hover{
	opacity: 1;
}
.citylist-item:nth-child(1) .itme-char{
	background-image: url(../../../../assets/img/city/char1.png);
}
.citylist-item:nth-child(2) .itme-char{
	background-image: url(../../../../assets/img/city/char2.png);
}
.citylist-item:nth-child(3) .itme-char{
	background-image: url(../../../../assets/img/city/char3.png);
}
</style>
