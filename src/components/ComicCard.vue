<template>
	<div class="comic-card">
		<div class="image-box">
			<img :src="comic.thumb" :alt="series" />
		</div>
		<div class="details">
			<p>{{ comic.series }}</p>
		</div>
	</div>
</template>

<script>
export default {
	name: 'ComicCard',
	props: {
		comic: Object,
	},
};
</script>

<style lang="scss" scoped>
@import '../assets/styles/mixins';
.comic-card {
	width: calc(100% / 6 - 20px);
	margin: 10px;
	@include center(both);
	flex-direction: column;
}
.image-box {
	max-width: 250px;
	aspect-ratio: 1;
	text-align: center;
	img {
		width: 100%;
		height: 100%;
		object-fit: cover;
		object-position: top;
	}
}
.details {
	text-transform: uppercase;
	height: 20px;
	font-size: 0.8rem;
	margin-top: 10px;
	text-align: center;
}
</style>
