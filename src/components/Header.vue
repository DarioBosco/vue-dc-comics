<template>
	<div class="header">
		<div class="logo">
			<img src="@/assets/img/dc-logo.png" alt="" />
		</div>
		<nav>
			<ul>
				<li v-for="(link, index) in links" :key="index"></li>
			</ul>
		</nav>
	</div>
</template>

<script>
import headerLinks from '@/assets/data/links.js';
export default {
	name: 'Header',
	data() {
		return {
			links: headerLinks,
		};
	},
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.header {
	display: flex;
}
ul {
	list-style: none;
	background: orange;
	li {
		display: inline-block;
		background: orangered;
	}
}
</style>
