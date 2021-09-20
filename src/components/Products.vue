<template>
	<div class="wrapper">
		<div class="container-fluid top">
			<div class="container">
				<h2>{{ message }}</h2>
			</div>
		</div>
		<div class="container-fluid bottom">
			<div class="container">
				<ul>
					<li v-for="(product, index) in products" :key="index">
						<div class="product_image">
							<img :src="require(`../assets/img/${product.category + product.item + product.extension}`)" />
						</div>
						<div class="product_text">
							{{ product.text }}
						</div>
					</li>
				</ul>
			</div>
		</div>
	</div>
</template>

<script>
import products from '@/assets/data/products.js';
export default {
	name: 'Products',
	data: function() {
		return {
			products: products.products,
			message: '--> Content goes here <---',
		};
	},
};
</script>

<style scoped lang="scss">
@import '../assets/styles/variables';

.wrapper {
	.container-fluid {
		height: 150px;
		width: 100vw;
		color: white;
		.container {
			width: 80%;
			height: 100%;
			margin: 0 auto;
			display: flex;
			align-items: center;
		}

		&.top {
			background-color: $secondary;
		}

		&.bottom {
			background-color: $primary;
			height: 100%;
			ul {
				height: 100%;
				list-style: none;
				li {
					height: 100%;
					display: inline-block;
					.product-image {
						height: 100%;
						img {
							height: 50%;
						}
					}
				}
			}
		}
	}
}
</style>
