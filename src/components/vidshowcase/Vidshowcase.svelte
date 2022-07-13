<script>
	import vid from '../../assets/videos/showcase.mp4';
</script>

<section class="banner">
	<!-- svelte-ignore a11y-media-has-caption -->
	<video muted autoplay loop controlsList="nodownload" oncontextmenu="return false;" playsinline>
		<source src={vid} type="video/mp4" />
	</video>
	<div class="content">
		<h1>Agli Studio</h1>
		<p>Ghana's Favorite</p>
	</div>
</section>

<style lang="scss">
	.banner {
		width: 100%;
		height: 100vh;
		overflow: hidden;
		display: flex;
		justify-content: center;
		align-items: center;
        
		video {
            position: absolute;
			top: 0;
			left: 0;
			object-fit: cover;
			width: 100%;
			height: 100%;
			pointer-events: none;
			opacity: 0.5;
		}
		.content {
            transition: 1s ease;
			position: relative;
			z-index: 1;
			text-align: center;
			h1 {
				font-size: 80px;
				color: white;
			}
			p {
				font-size: 40px;
				color: white;
			}
		}
	}

	// media query
	@media (max-width: 992px) {
        .banner {
			.content {
				h1 {
					font-size: 50px;
				}
				p {
					font-size: 25px;
					color: white;
				}
			}
		}
	}
	@media (max-width: 688px) {
		.banner {
			.content {
				h1 {
					font-size: 40px;
				}
				p {
					font-size: 20px;
					color: white;
				}
			}
		}
	}
</style>
