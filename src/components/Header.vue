//TODO: Aggiungere la classe "active" dinamica.

<template>
	<div class="header">
		<div class="logo">
			<img src="@/assets/img/dc-logo.png" alt="" />
		</div>
		<nav>
			<ul>
				<li v-for="(link, index) in links" :key="index" :class="link.current ? 'active' : null">
					<a :href="link.link">{{ link.text }}</a>
				</li>
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
			links: headerLinks.headerLinks,
		};
	},
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '../assets/styles/variables';
.header {
	margin-top: 20px;
	display: flex;
	justify-content: space-between;
	align-items: center;
	height: 100%;
	.logo {
		height: 100%;
	}
	nav {
		ul {
			list-style: none;
			li {
				display: inline-block;
				text-transform: uppercase;
				margin-left: 25px;

				a {
					text-decoration: none;
					color: inherit;
				}

				&.active {
					color: $primary;
					border-bottom: 5px solid $primary;
				}
			}
		}
	}
}
</style>
