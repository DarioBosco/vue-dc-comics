<template>
	<div class="container-fluid">
		<div class="container">
			<div class="logo">
				<img src="@/assets/img/dc-logo.png" alt="" />
			</div>
			<nav>
				<ul>
					<li v-for="(link, index) in links" :key="index" :class="link.current ? 'active' : null" @click="selectCurrentElement(link)">
						<a :href="link.link">{{ link.text }}</a>
					</li>
				</ul>
			</nav>
		</div>
	</div>
</template>

<script>
import links from '@/assets/data/links.js';
export default {
	name: 'Header',
	activeElement: 0,
	data() {
		return {
			links: links.headerLinks,
		};
	},
	methods: {
		selectCurrentElement(element) {
			this.links.forEach((i) => {
				i.current = false;
			});
			element.current = true;
		},
	},
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '../assets/styles/variables';
.container-fluid {
	width: 100vh;
	.container {
		width: 80%;
		margin: 0 auto;
		display: flex;
		justify-content: space-between;
		align-items: center;
		height: 100px;
		.logo {
			height: 100%;
			img {
				width: 75%;
				position: relative;
				top: 50%;
				left: 50%;
				transform: translate(-50%, -50%);
			}
		}
		nav {
			height: 100%;
			ul {
				height: 100%;
				display: flex;
				align-items: center;
				list-style: none;
				li {
					height: 100%;
					display: flex;
					align-items: center;
					text-transform: uppercase;
					margin-left: 25px;
					border-bottom: 3px solid transparent;

					a {
						text-decoration: none;
						color: inherit;
					}

					&.active {
						color: $primary;
						border-bottom: 3px solid $primary;
					}
				}
			}
		}
	}
}
</style>
