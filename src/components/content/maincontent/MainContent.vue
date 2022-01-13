<template>
	<div class="content-wrop">
		<poster></poster>
		<news></news>
		<city></city>
		<social></social>
		<attention></attention>
		<foot></foot>
	</div>
</template>

<script>
	import Poster from './poster/Poster.vue'
	import News from './news/News.vue'
	import City from './city/City.vue'
	import Social from './social/Social.vue'
	import Attention from './social/Attention.vue'
	import Foot from './foot/Foot.vue'
	
	export default {
		name: 'MainContent',
		components: {
			Poster,
			News,
			City,
			Social,
			Attention,
			Foot
		}
	}
	

</script>

<style>
.content-wrop{
	z-index: 1;
}
</style>
