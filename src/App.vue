<template>
	<div id="app">
		<Header />
		<Products />
		<Footer />

	</div>
</template>

<script>
import Header from './components/Header.vue';
import Products from './components/Products.vue';
import Footer from './components/Footer.vue';

export default {
	name: 'App',
	components: {
		Header,
		Products,
		Footer,
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
}
</style>
