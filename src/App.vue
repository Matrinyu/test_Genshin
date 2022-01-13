<template>
  <div id="app">
		<head-bar></head-bar>
		<main-content></main-content>
  </div>
</template>

<script>
	import HeadBar from './components/content/headbar/HeadBar.vue'
	import MainContent from './components/content/maincontent/MainContent.vue'
	
	export default {
	  name: 'app',
	  components: {
			HeadBar,
			MainContent
	  }
	}

</script>

<style>	
*{
	margin: 0;
	padding: 0;
}
</style>
