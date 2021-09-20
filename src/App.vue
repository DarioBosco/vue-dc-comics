<template>
	<div id="app">
		<Header />
		<Products />
	</div>
</template>

<script>
import Header from './components/Header.vue';
import Products from './components/Products.vue';

export default {
	name: 'App',
	components: {
		Header,
		Products,
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
}
</style>
