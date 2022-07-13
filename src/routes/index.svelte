<script>
	import { fly } from 'svelte/transition';
	import Showcase from '../components/home/ShowCaseHome.svelte';
	import VideoShowcase from '../components/vidshowcase/Vidshowcase.svelte';
	import SocialMedia from '../components/socialmedia/Socialmedia.svelte';
</script>

<svelte:head>
	<title>AGLISTUDIO | Home</title>
</svelte:head>

<section
	class="home-index"
	in:fly={{ y: 50, duration: 500, delay: 500 }}
	out:fly={{ duration: 500 }}
>
	<SocialMedia />
	<VideoShowcase />
</section>
