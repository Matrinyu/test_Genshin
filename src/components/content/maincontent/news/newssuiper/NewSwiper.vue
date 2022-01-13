<template>
	<div class="shell">
		<ul class="images">
			<li class="img"></li>
			<li class="img"></li>
			<li class="img"></li>
			<li class="img"></li>
		</ul>
		<ul class="min-button">
			<li class="min"></li>
			<li class="min"></li>
			<li class="min"></li>
			<li class="min"></li>
		</ul>
	</div>
</template>

<script>
	export default {
		name: 'newswiper',
	}
	
	window.addEventListener('load', function(){
		let images = document.querySelector('.images')
		let min = document.querySelectorAll('.min')
		
		let index = 0
		let time = 0
		
		//改变image位置用index定位在第几幅图
		function position(){
			images.style.left = (index * -100) + "%"
			for(let j = 0; j < min.length; j++){
				min[j].style.backgroundColor = 'transparent'
			}
			min[index].style.backgroundColor = '#ffffff'
		}
		//确定index的值，如果大于最后一幅图则清零，使之回到第一幅
		function add(){
			if(index >= min.length-1){
				index = 0
			}else{
				index++
			}
		}
		//确定index的值，如果小于第一幅图则清零，使之回到最后一幅
		function desc(){
			if(index < 1){
				index = min.length-1
			}else{
				index--
			}
		}
		//立即执行定时器
		(function timer(){
			time = setInterval(() =>{
				add()
				position()
			},2500)
		})()
		//定时器
		function timer(){
			time = setInterval(() =>{
				add()
				position()
			},2500)
		}
		//利用for循环添加点击事件,同时用改变现实位置,并重新启动定时器
		for(let i = 0; i < min.length; i++){
			min[i].onclick = function(){
				index = i
				for(let j = 0; j < min.length; j++){
					min[j].style.backgroundColor = 'transparent'
				}
				min[i].style.backgroundColor = '#ffffff'
				position()
				clearInterval(time)
				timer()
			}	
		}
	})
</script>

<style>
.shell {
	width: 100%;
	height: 100%;
	position: relative;
	overflow-x: hidden;
}
.images{
	width: 400%;
	height: 100%;
	display: flex;
	position: absolute;
	left: 0;
	transition: .3s;
	list-style: none;
}
.img{
	width: 100%;
	background-size: 640px 400px;
}
.img:nth-child(1){
	background-image: url(../../../../../assets/img/news/前瞻特别节.jpg);
}
.img:nth-child(2){
	background-image: url(../../../../../assets/img/news/阿贝多.jpg);
}
.img:nth-child(3){
	background-image: url(../../../../../assets/img/news/尤拉.png);
}
.img:nth-child(4){
	background-image: url(../../../../../assets/img/news/蒙德茶会.jpg);
}
.min-button{
	width: 100%;
	position: absolute;
	display: flex;
  align-items: flex-end;
  justify-content: center;
	left: 0;
	bottom: 15px;
	z-index: 90;
	right: 5%;
}
.min{
	width: 18px;
	height: 18px;
	background-color: rgba(0,0,0,0.1);
	border-radius: 50%;
	border: solid 2px rgba(255,255,255,0.3);
	box-shadow: 0 0 12px 0 rgb(17 17 17 / 30%);
	opacity: 1;
	margin: 5px;
	cursor: pointer;
}
.min:nth-child(1){
	background-color: #ffffff;
}
</style>
