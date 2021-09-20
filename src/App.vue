<template>
	<div id="app">
		<Header />
	</div>
</template>

<script>
import Header from './components/Header.vue';

export default {
	name: 'App',
	components: {
		Header,
	},
};
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Roboto&display=swap');
#app {
	font-family: Roboto, sans-serif;
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
	color: #2c3e50;
	width: 80%;
	margin: 0 auto;
}
</style>
