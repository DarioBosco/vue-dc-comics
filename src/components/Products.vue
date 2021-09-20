<template>
	<div class="container-fluid">
		<div class="container">
			<h2>{{ message }}</h2>
		</div>
	</div>
</template>

<script>
export default {
	name: 'Products',
	data: function() {
		return {
			message: '--> Content goes here <---',
		};
	},
};
</script>

<style scoped lang="scss">
@import '../assets/styles/variables';
.container-fluid {
	height: 150px;
	width: 100vw;
	background-color: $secondary;
	color: white;
	.container {
		height: 100%;
		width: 80%;
		margin: 0 auto;
		display: flex;
		align-items: center;
	}
}
</style>
