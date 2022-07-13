<script>
	import { fly } from 'svelte/transition';
	import pic from '../assets/images/company1.jpg';
	import pic1 from '../assets/images/company6.jpg';
</script>

<svelte:head>
	<title>Gallery</title>
</svelte:head>
<section
	in:fly={{ y: 50, duration: 500, delay: 500 }}
	out:fly={{ duration: 500 }}
	class="gallery-container"
>
	<a href="/pictures">
		<div class="gallery-box">
			<img src={pic} alt="" />
			<h4>Pictures</h4>
		</div>
	</a>
	<a href="/videos">
		<div class="gallery-box">
			<img src={pic1} alt="" />
			<h4>Videos</h4>
		</div>
	</a>
</section>

<style lang="scss">
	.gallery-container {
		display: flex;
		justify-content: center;
		align-items: center;
		gap: 1rem;
		flex-wrap: wrap;
		margin-top: 120px;
		padding: 20px;
		
		.gallery-box {
			transition: 1s ease;
			padding: 20px;
			cursor: pointer;
			width: 500px;
			height: 500px;
			border-radius: 20px;
			display: flex;
			flex-direction: column;
			gap: 1rem;
			justify-content: center;
			align-items: center;

			img {
				width: 100%;
				border-radius: 20px;
			}
			h4 {
				color: white;
				font-size: 20px;
				line-height: 1.1666666667;
				letter-spacing: 0.009em;
			}
		}
	}

	// media queries
	@media (max-width: 992px) {
		.gallery-container {
			.gallery-box {
				width: 450px;
				height: 450px;
			}
		}
	}
	@media (max-width: 668px) {
		.gallery-container {
			.gallery-box {
				width: 400px;
				height: 400px;
			}
		}
	}
</style>
