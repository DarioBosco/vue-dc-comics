<template>
	<div class="footer">
		<div class="footer-top">
			<div class="footer-links">
				<ul class="footer-links-list" v-for="(link, index) in links" :key="index">
					<li class="list-title">{{ link.category }}</li>
					<li class="list-item" v-for="(item, index) in link.items" :key="index">
						<a class="list-link" :href="item.link">{{ item.text }}</a>
					</li>
				</ul>
			</div>
			<div class="image-box">
				<img src="../assets/img/dc-logo-bg.png" alt="" />
			</div>
		</div>
	</div>
</template>

<script>
import footerLinks from '@/assets/data/links.js';
export default {
	name: 'Header',
	data() {
		return {
			links: footerLinks.footerLinks,
		};
	},
};
</script>

<style lang="scss" scoped>
.footer {
	height: 500px;
	width: 100vw;
	background-image: url('../assets/img/footer-bg.jpg');
	background-size: cover;

	.footer-top {
		width: 80%;
		height: 100%;
		margin: 0 auto;
		color: white;
		display: flex;
		justify-content: space-between;
		.footer-links {
			width: 30%;
			height: 100%;
			display: flex;
			flex-direction: column;
			flex-wrap: wrap;

			.footer-links-list {
				width: 30%;

				.list-title {
					font-size: 1.5rem;
					margin: 20px 0;
					font-weight: bold;
				}
				.list-item {
					margin: 0.3rem;
					color: grey;
				}
			}
		}
		.image-box {
			width: 600px;
			height: 100%;
			/* overflow: hidden; */
			img {
				width: 100%;
				height: 100%;
				object-fit: cover;
			}
		}
	}
}

ul {
	list-style: none;
}
a {
	color: inherit;
	text-decoration: none;
}
</style>
