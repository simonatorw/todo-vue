<template>
	<div id="app">
		<hello-world />
		<!-- <router-view/> -->
	</div>
</template>

<script>
	import HelloWorld from '@/components/HelloWorld';

	export default {
		name: 'app',
		components: {
			'hello-world': HelloWorld
		}
	};
</script>

<style>
	#app {
		font-family: 'Avenir', Helvetica, Arial, sans-serif;
		-webkit-font-smoothing: antialiased;
		-moz-osx-font-smoothing: grayscale;
		color: #2c3e50;
		margin: 10px;
	}
</style>
