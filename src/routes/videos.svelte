<script context="module">
	export async function load({ fetch }) {
		const prductionVideos = await fetch(`https://aglistudiosgh.xyz/pro_vids/`, {
			headers: {
				'content-type': 'application/json',
				accept: 'application/json'
			}
		});
		const proVids = await prductionVideos.json();

		if (prductionVideos.ok) {
			return {
				props: {
					proVids
				}
			};
		}
	}
</script>

<script>
	export let proVids;

	import { fly } from 'svelte/transition';
	import playButton from '../assets/images/icons/play-button.png';
	let playButtonClicked = false;
	let openModalVideo = false;
	let videoModal = '';
	let canDownload = 'nodownload';

	const handlePlayButton = () => {
		playButtonClicked = true;
	};
	const handleCloseVideoContainer = () => {
		playButtonClicked = false;
	};
	function openModal(src) {
		playButtonClicked = true;
		openModalVideo = true;
		videoModal = src;
	}
</script>

<section
	class="gallery-container"
	in:fly={{ y: 50, duration: 500, delay: 500 }}
	out:fly={{ duration: 500 }}
>
	{#if playButtonClicked}
		<section class="video-container" on:click={handleCloseVideoContainer}>
			<!-- svelte-ignore a11y-media-has-caption -->
			<video
				playsinline
				controls
				controlsList={canDownload}
				autoplay="true"
				width="80%"
				height="80%"
				oncontextmenu="return false;"
			>
				<source src={videoModal} type="video/mp4" />
			</video>
		</section>
	{/if}
	<div class="video-box">
		{#each proVids as vid}
			<div class="box">
				<!-- svelte-ignore a11y-media-has-caption -->
				<video
					oncontextmenu="return false;"
					controlsList="nodownload"
					on:click={(e) => openModal(vid.get_video)}
				>
					<source src={vid.get_video} type="video/mp4" />
				</video>
			</div>
		{/each}
	</div>
</section>

<style lang="scss">
	.gallery-container {
		.video-container {
			top: 0;
			position: fixed;
			width: 100%;
			height: 100%;
			background-color: rgba(0, 0, 0, 0.8);
			z-index: 1000;
			display: flex;
			justify-content: center;
			align-items: center;
			gap: 1rem;
			cursor: pointer;
			video {
				border-radius: 24px;
				outline: none;

				border: none;
			}
			// .closebut {
			// 	color: #c8a461;
			// 	font-size: 50px;
			// 	cursor: pointer;
			// 	transition: ease 0.5s;
			// 	&:hover {
			// 		transform: rotate(90deg);
			// 	}
			// }
		}
		.video-box {
			display: flex;
			justify-content: center;
			flex-wrap: wrap;

			.box{
				height:15rem;
				width: 25rem;
				margin: 2rem;
				overflow: hidden;
				border-radius: 1rem;
				video{ 
					height:100%;
					width:100%;
					object-fit:cover;
					outline: none;
					border: none;
					cursor: pointer;
					&:hover{
						transition: 1s linear;
						transform: scale(1.3);
					}
				}
			}
		}
	}

	@media (max-width: 992px) {
		.gallery-container {
			.gallery-box {
			}
		}
	}
	@media (max-width: 5668px) {
	}
</style>
