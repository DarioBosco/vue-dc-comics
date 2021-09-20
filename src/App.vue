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
@import './assets/styles/common';
@import './assets/styles/variables';
#app {
	font-family: Roboto, sans-serif;
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
	color: #2c3e50;
	width: 80%;
	margin: 0 auto;
}
</style>
