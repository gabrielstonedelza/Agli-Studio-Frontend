<script>
	import Logo from '../assets/images/companylogo.png';
	import layout from '../styles/layout/layout.css';
	import facebook from '../assets/images/icons/facebook.png';
	import instagram from '../assets/images/icons/instagram.png';
	import twitter from '../assets/images/icons/twitter.png';
	import youtube from '../assets/images/icons/youtube.png';
	import globalcss from "../styles/global.css"
	import gallery from "../styles/gallery/gallery.css"
	import menuPic from "../assets/images/icons/menu.png"

	let sideNavOpened = false;
	const handleOpenedSideNav = () => {
		sideNavOpened = true;
	};
	const handleClosedSideNav = () => {
		sideNavOpened = false;
	};
</script>

<div class="maincontainer">
	<div class="mainnavitems">
		<div class="title">
			<img src={Logo} alt="" />
		</div>

		<div class="menulinks">
			<div class="navbarlink">
				<a href="/">Home</a>
			</div>
			<div class="navbarlink">
				<a href="/explore">Explore</a>
			</div>
			<div class="navbarlink">
				<a href="/movies" passHref> Movies </a>
			</div>
			<!-- <div class="navbarlink">
				<a href="/television" passHref> Television </a>
			</div> -->
			<div class="navbarlink">
				<a href="/gallery" passHref> Gallery </a>
			</div>
			<div class="navbarlink">
				<a href="/about" passHref> About </a>
			</div>
		</div>

		<div class="bars">
			<img src={menuPic} alt="" on:click={handleOpenedSideNav}>
		</div>
	</div>
</div>

{#if sideNavOpened}
	<div on:click={handleClosedSideNav}>
		
		<div class="onsmallerscreen">
			<div class="mainnavitems">
				<!-- <p class="close" on:click={handleClosedSideNav}>X</p> -->
				<div class="title">
					<img src={Logo} alt="" />
				</div>

				<div class="menulinks">
					<div class="navbarlink">
						<a href="/">Home</a>
					</div>
					<div class="navbarlink">
						<a href="/explore">Explore</a>
					</div>
					<div class="navbarlink">
						<a href="/movies" passHref> Movies </a>
					</div>
					<div class="navbarlink">
						<a href="/gallery" passHref> Gallery </a>
					</div>
					<div class="navbarlink">
						<a href="/about" passHref> About </a>
					</div>
				</div>
			</div>
		</div>
	</div>
{/if}

<br />
<br />
<br />

<slot></slot>