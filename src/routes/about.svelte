<script>
	import { fly } from 'svelte/transition';

	import pic9 from '../assets/images/9.jpg';
	import pic10 from '../assets/images/pexels-luis-quintero-1787220.jpg'
	import pic11 from '../assets/images/pexels-mentatdgt-1078744.jpg';
	import pic12 from '../assets/images/pexels-kaique-rocha-243757.jpg';
	import email from '../assets/images/icons/mail.png';
	import phone from '../assets/images/icons/phone-call.png';
	import location from '../assets/images/icons/location-1.png';
	import pic13 from "../assets/images/pexels-obregonia-d-toretto-918281.jpg"
</script>

<svelte:head>
	<title>AGLI | About</title>
</svelte:head>

<section class="about" in:fly={{ y: 50, duration: 500, delay: 500 }} out:fly={{ duration: 500 }}>
	<div class="about-showcase">
		<div class="about-showcase-content">
			<h2>About US</h2>
		</div>
	</div>
	<div class="container">
		<div class="pcontainer">
			<p>
				Agli Ventures is in Accra - Ghana based company whose principal activities include
				(videography and photography production,music production and event management.). Agli
				Ventures(Agli Studio) is registered under the laws of Ghana(2013) and since announcing our
				presence in the video and photography industry,we have been able to march up and benn
				dynamic in our way of execution to meet the quality standard of today's modern technology
				world with execellence. Our biggest joy is to see our clients been satisfied to the maximum
				in all ways.
			</p>
		</div>
		<h2>Portfolio</h2>
		<div class="portfolio">
			<div class="portfolio-pic">
				<img src={pic9} alt="" />
			</div>
			<div class="portfolio-content">
				<p>
					Worked with the Ministry of Education in Ghana. (Produce and shoot free SHS Video Advert
					and Radio Voice recording advert.
				</p>
				<p>
					Worked with eagle productions limited and mobikefliks to produce and shoot a television
					series tittle "we2".
				</p>
				<p>Worked with medlab Ghana a producer for “how clean is your house”</p>
			</div>
		</div>
		<h2>Our Services</h2>
		<div class="services">
			<div class="service-box">
				<img src={pic10} alt="" />
				<h4>Photography</h4>
			</div>
			<div class="service-box">
				<img src={pic11} alt="" />
				<h4>Designing and Printing</h4>
			</div>
			<div class="service-box">
				<!-- svelte-ignore a11y-media-has-caption -->
				<img src={pic12} alt="" />
				<h4>Videography</h4>
			</div>
			<div class="service-box">
				<!-- svelte-ignore a11y-media-has-caption -->
				<img src={pic13} alt="" />
				
				<h4>Film Production</h4>
			</div>
		</div>
		<footer class="footer">
			<h2>Let's do Business</h2>
			<div class="footer-container">
				<div class="contact">
					<div class="contact-box">
						<img src={email} alt="" /> :
						<p>info@aglistudiosgh.com</p>
					</div>
					<div class="contact-box">
						<img src={phone} alt="" /> :
						<p>
							0244800896 / 0574900402 <br />
							O557629434/0203946610
						</p>
					</div>
					<div class="contact-box">
						<img src={location} alt="" /> :
						<p>Accra,Ghana</p>
					</div>
				</div>
			</div>
			<div class="main-footer">
				&copy 2022 Agli studiosgh.All Rights Reserved. Designed by Havens Software
			</div>
		</footer>
	</div>
</section>

<style lang="scss">
	.about {
		h2 {
			color: white;
			text-align: center;
			padding: 20px;
			font-size: 30px;
		}
		.about-showcase {
			display: flex;
			justify-content: center;
			align-items: center;
			width: 100%;
			height: 50vh;
			background: url('../assets//images//pexels-md-iftekhar-uddin-emon-403495.jpg');
			background-position: center;
			background-size: cover;
			background-repeat: no-repeat;
			background-attachment: fixed;

			.about-showcase-content {
				h2 {
					color: white;
					font-size: 60px;
				}
			}
		}
		.container {
			display: flex;
			flex-direction: column;
			gap: 1rem;
			.pcontainer {
				margin-top: 20px;
				width: 80%;
				// text-align: center;
				margin: 0 auto;
				padding: 20px;
				display: flex;
				justify-content: center;
				align-items: center;

				p {
					color: white;
					font-size: 24px;
					line-height: 1.1666666667;
					letter-spacing: 0.009em;
				}
			}
			.portfolio {
				width: 80%;
				// text-align: center;
				margin: 0 auto;
				display: flex;
				gap: 1rem;
				justify-content: center;
				align-items: center;
				padding: 20px;
				.portfolio-pic {
					// width: 100%;
					img {
						width: 400px;
						height: 100%;
					}
				}
				.portfolio-content {
					p {
						color: white;
						font-size: 24px;
						line-height: 1.1666666667;
						letter-spacing: 0.009em;
					}
				}
			}
			.services {
				width: 80%;
				// text-align: center;
				margin: 0 auto;
				display: grid;
				grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
				gap: 1rem;
				.service-box {
					h4 {
						color: white;
						font-size: 24px;
						line-height: 1.1666666667;
						letter-spacing: 0.009em;
						text-align: center;
					}
					img {
						width: 100%;
						height: 200px;
						border-radius: 20px;
					}
					
				}
			}
			.footer {
				.contact {
					display: flex;
					justify-content: center;
					align-items: center;
					gap: 1rem;
					.contact-box {
						display: flex;
						flex-direction: column;
						justify-content: center;
						align-items: center;
						img {
							width: 40px;
							height: 40px;
						}
						p {
							color: white;
							font-size: 20px;
							line-height: 1.1666666667;
							letter-spacing: 0.009em;
						}
					}
				}
				.main-footer {
					width: 100%;
					background-color: rgb(0, 0, 0);
					display: flex;
					justify-content: center;
					align-items: center;
					padding: 20px;
					color: white;
					font-size: 15px;
					line-height: 1.1666666667;
					letter-spacing: 0.009em;
				}
			}
		}
	}

	// media queries
	@media (max-width: 992px) {
		.about-showcase {
			display: flex;
			justify-content: center;
			align-items: center;
			width: 100%;
			height: 50vh;
			background: url('../assets//images//pexels-md-iftekhar-uddin-emon-403495.jpg');
			background-position: center;
			background-size: cover;
			background-repeat: no-repeat;
			background-attachment: fixed;

			.about-showcase-content {
				h2 {
					color: white;
					font-size: 60px;
				}
			}
		}
		.container {
			display: flex;
			flex-direction: column;
			gap: 1rem;
			.pcontainer {
				margin-top: 20px;
				width: 80%;
				// text-align: center;
				margin: 0 auto;
				padding: 20px;
				display: flex;
				justify-content: center;
				align-items: center;

				p {
					color: white;
					font-size: 24px;
					line-height: 1.1666666667;
					letter-spacing: 0.009em;
				}
			}
			.portfolio {
				width: 80%;
				// text-align: center;
				margin: 0 auto;
				display: flex;
				gap: 1rem;
				justify-content: center;
				align-items: center;
				padding: 20px;
				.portfolio-pic {
					// width: 100%;
					img {
						width: 100%;
						height: 100%;
					}
				}
				.portfolio-content {
					p {
						color: white;
						font-size: 20px;
						line-height: 1.1666666667;
						letter-spacing: 0.009em;
					}
				}
			}
			.services {
				width: 80%;
				// text-align: center;
				margin: 0 auto;
				display: grid;
				grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
				gap: 1rem;
				.service-box {
					h4 {
						color: white;
						font-size: 24px;
						line-height: 1.1666666667;
						letter-spacing: 0.009em;
						text-align: center;
					}
					img {
						width: 100%;
						height: 250px;
					}
				}
			}
			.footer {
				.contact {
					display: flex;
					justify-content: center;
					align-items: center;
					gap: 1rem;
					.contact-box {
						display: flex;
						flex-direction: column;
						justify-content: center;
						align-items: center;
						img {
							width: 40px;
							height: 40px;
						}
						p {
							color: white;
							font-size: 20px;
							line-height: 1.1666666667;
							letter-spacing: 0.009em;
						}
					}
				}
				.main-footer {
					width: 100%;
					background-color: rgb(0, 0, 0);
					display: flex;
					justify-content: center;
					align-items: center;
					padding: 20px;
					color: white;
					font-size: 15px;
					line-height: 1.1666666667;
					letter-spacing: 0.009em;
				}
			}
		}

	}
	@media (max-width: 668px) {
		.about {
			h2 {
				color: white;
				text-align: center;
				padding: 20px;
				font-size: 25px;
			}
			.about-showcase {
				.about-showcase-content {
					h2 {
						color: white;
						font-size: 40px;
					}
				}
			}
			.container {
				.pcontainer {
					margin-top: 20px;
					width: 80%;
					margin: 0 auto;
					padding: 20px;
					display: flex;
					justify-content: center;
					align-items: center;

					p {
						color: white;
						font-size: 18px;
						line-height: 1.1666666667;
						letter-spacing: 0.009em;
					}
				}
				.portfolio {
					width: 80%;
					margin: 0 auto;
					display: flex;
					flex-direction: column;
					gap: 1rem;
					justify-content: center;
					align-items: center;
					padding: 20px;
					.portfolio-pic {
						// width: 100%;
						img {
							width: 100%;
							height: 100%;
						}
					}
					.portfolio-content {
						p {
							color: white;
							font-size: 18px;
							line-height: 1.1666666667;
							letter-spacing: 0.009em;
						}
					}
				}
				.services {
					.service-box {
						h4 {
							color: white;
							font-size: 20px;
							line-height: 1.1666666667;
							letter-spacing: 0.009em;
							text-align: center;
						}
						img {
							width: 100%;
							// he/ight: 250px;
						}
					}
				}
				.footer {
				.contact {
					display: flex;
					justify-content: center;
					align-items: center;
					flex-direction: column;
					gap: 1rem;
					padding: 1rem;
					.contact-box {
						display: flex;
						flex-direction: column;
						justify-content: center;
						align-items: center;
						img {
							width: 40px;
							height: 40px;
						}
						p {
							color: white;
							font-size: 18px;
							line-height: 1.1666666667;
							letter-spacing: 0.009em;
						}
					}
				}
				.main-footer {
					width: 100%;
					background-color: rgb(0, 0, 0);
					display: flex;
					justify-content: center;
					align-items: center;
					padding: 20px;
					color: white;
					font-size: 12px;
					line-height: 1.1666666667;
					letter-spacing: 0.009em;
				}
			}
			}
		}
	}
</style>
