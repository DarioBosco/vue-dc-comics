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
		<div class="footer-bottom">
			<div class="content">
				<div class="button">
					<button>SIGN UP NOW!</button>
				</div>
				<div class="socials">
					<div class="follow-us">FOLLOW US</div>
					<ul>
						<li v-for="(social, index) in socials" :key="index">
							<div class="social-box">
								<img :src="require(`../assets/${social.icon}`)" />
							</div>
						</li>
					</ul>
				</div>
			</div>
		</div>
	</div>
</template>

<script>
import footerLinks from '@/assets/data/links.js';
import socials from '@/assets/data/socials.js';
export default {
	name: 'Header',
	data() {
		return {
			links: footerLinks.footerLinks,
			socials: socials,
		};
	},
};
</script>

<style lang="scss" scoped>
@import '../assets/styles/variables';
@import '../assets/styles/mixins';
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
	.footer-bottom {
		width: 100vw;
		height: 30%;
		background-color: $secondary;

		.content {
			width: 80%;
			height: 100%;
			margin: 0 auto;
			display: flex;
			justify-content: space-between;
			align-items: center;

			.button {
				@include center(vertical);

				button {
					height: 50px;
					width: 200px;
					background: transparent;
					border: 2px solid $primary;
					color: white;
					font-size: 1.2rem;
					font-weight: bold;
				}
			}

			.socials {
				@include center(vertical);
				.follow-us {
					color: $primary;
					font-size: 1.2rem;
					font-weight: bold;
				}

				li {
					display: inline-block;
					margin-left: 20px;

					.social-box {
						height: 35px;
						width: 35px;

						img {
							width: 100%;
						}
					}
				}
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
