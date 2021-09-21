<template>
	<div class="wrapper">
		<div class="container-fluid top">
			<div class="container"></div>
		</div>
		<div class="container-fluid bottom">
			<div class="container">
				<ul>
					<li v-for="(product, index) in products" :key="index">
						<div class="product-image">
							<img :src="require(`../assets/img/${product.category + product.item + product.extension}`)" />
						</div>
						<div class="product-text">
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
		};
	},
};
</script>

<style scoped lang="scss">
@import '../assets/styles/variables';
@import '../assets/styles/mixins';

.wrapper {
	.container-fluid {
		height: 150px;
		width: 100vw;
		color: white;
		.container {
			width: 80%;
			height: 100%;
			margin: 0 auto;
			@include center(vertical);
		}

		&.top {
			background-color: $secondary;
		}

		&.bottom {
			background-color: $primary;
			height: 150px;
			ul {
				height: 100%;
				width: 100%;
				list-style: none;
				@include center(vertical);
				justify-content: space-around;
				li {
					height: 100%;
					width: calc(100% / 5);
					display: inline-block;
					@include center(both);
					.product-image {
						height: 60px;
						width: 60px;
						@include center(both);
						margin-right: 20px;
						img {
							height: 100%;
						}
					}
					.product-text {
						text-transform: uppercase;
					}
				}
			}
		}
	}
}
</style>
