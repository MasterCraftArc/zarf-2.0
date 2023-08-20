<script>
	import Card from '../components/Card.svelte';
	import Home from '../components/Home/Home.svelte';
	import Navbar from '../components/Navbar/Navbar.svelte';
	import Blob from '../components/blob/Blob.svelte';
	import webSecure from '../assets/png/cloud-icons/web-security.png';
	import '../styles/global.css';
	import wireLessCloud from '../assets/png/cloud-icons/wireless-cloud.png';
	import server from '../assets/png/cloud-icons/server.png';
	import Columns from '../components/Columns/Columns.svelte';
	import rocket from '../assets/png/zarf-rocket.png';
	import nuclear from '../assets/png/zarf-nuclear.png';
	import Column from '../components/Columns/Column.svelte';
	import sub from '../assets/png/zarf-sub.png';
	import Cards from '../components/Cards.svelte';
	import community from '../assets/png/cloud-icons/community.png';
	import hosting from '../assets/png/cloud-icons/hosting.png';
	import pieces from '../assets/png/cloud-icons/pieces.png';
	import document from '../assets/png/cloud-icons/document.png';
	import StatsCard from '../components/statsCard/StatsCard.svelte';
	import Footer from '../components/footer/Footer.svelte';
	import Defense from '../components/Defense.svelte';
	import AirplaneMode from '../components/AirplaneMode.svelte';
	import { onMount } from 'svelte';
	import plane from '../assets/png/jet-plane.png'
	let isMobile = false;

	onMount(() => {
		window.addEventListener('resize', handleResize);
		handleResize();
	});

	function handleResize() {
		isMobile = window.innerWidth <= 992;
	}
</script>

<div class="container">
	<Home />

	<div class="cardHolder">
		<h1>Use LeapfrogAI for</h1>
		<div class="Card" class:mobileLayout={!isMobile}>
			<Card img={webSecure} heroText='Generative AI for Airgapped Systems'
				text="LeapfrogAI mirrors OpenAI and Hugging Face API surface so secure and disconnected enviroments can have a ChatGPT like experience while fully disconnected from the internet" />

			<Card img={wireLessCloud} heroText='Vector Databases & Embedding Creation'
				text='LeapfrogAI has efficent similarity searches on large scale databases and generative embeddings wich can be used for semantic similarity, clustering and more' />
			<Card img={server} heroText='Fine Tune Custom Models'
				text='LeapfrogAI has the ability to leverage customer specific data to fine-tune models that enable the AI to better understand your domain and provide more accurate contextal outputs' />
		</div>
	</div>


	<div class="blob2"><AirplaneMode /></div>

	<Columns HeroText='Sometimes Disconnected'
		text='Some systems experience disconnection occasionally due to temporary loss of access, like a rocket going around the moon. LeapfrogAI keeps these systems running.' img={rocket} />

	<Column HeroText='Always Disconnected'
		text='Other systems are always disconnected due to lack of internet access. Maybe they are underground, underwater, or on another planet.' img={sub} />

	<Columns HeroText='Disconnected in Emergencies'
		text="The world's most important infrastructure needs to be able to control their connection to the internet and still run in the case of internet loss or a cyber attack." img={plane} />


		<div class="cardText">
			<h1 class="secondHead">Why use LeapfrogAI</h1>
	<div class="CardsContainer">
		<div class="Cards">
			<Cards img={community} heroText='Free and Open Source Solution'
				text="Source code is free and open source on Apache 2 license. Enterprise support is available from Defense for interested organizations." />

			<Cards img={pieces} heroText='Install Packages with 3 Commands'
				text="Instalation is easy in any environment, including disconnected systems, by simplifying the installation of packages to just three steps." />
		</div>

		<div class="Cards">
			<Cards img={hosting} heroText='Built to Be Distro
			Agnostic'
				text="LeapfrogAI is k8s distro agnostic. With  support for K3s, K3d, and Kind. Is also compatible with EKS, AKS, GKE, RKE2 and many others distro services." />

			<Cards img={document} heroText='Deploy Across Environments'
				text="Ensures that applications are deployed the same way each time, whether deployed to a different cluster, machine or environment." />
		</div>

		<div class="Cards">
			<Cards img={pieces} heroText='Automats SBOM Generation'
				text="Automatically generated SBOM from the images contained within the zarf package of LeapfrogAI in compliance with federal mandates." />

			<Cards img={server} heroText='Multi Modal Generative AI'
				text="Combine multiple types of LLMS to enhance mission capabilities through text, speech to text, language translation, or many other generative AI modes " />
		</div>
	</div>
	</div>
	<StatsCard />
	<Defense />
	<Footer />
</div>

<style>
	.container {
		display: flex;
		flex-direction: column;
		align-items: center;
		margin: none;
		max-width: none;
	}

	.Card {
		display: flex;
	}



	.CardsContainer {
		display: flex;
		flex-wrap: wrap;
		justify-content: center;
		align-items: center;
		text-align: center;
		margin: 0;
	}

	.cardText{
		text-align: center;
	}

	.cardHolder {
		margin-top: 42em;
		text-align: center;
		display: flex;
		align-items: center;
		justify-content: center;
		flex-direction: column;
	}

	.Cards {
		display: flex;
		flex-wrap: wrap;
		justify-content: center;
		align-items: center;
		margin: 10px;
		flex-basis: 300px;
		max-width: 400px;
	}

	h1{
	font-family: "M PLUS Rounded 1c";
    font-weight: 300;
    font-size: 3.75rem;
    line-height: 1.2;
	margin-bottom: 3rem;
	margin-top: 4em;
	}

	.secondHead{
		margin-top: 4rem;
		margin-bottom: 0rem;
	}

	@media screen and (min-width: 1072px){
		h1{
			margin-top: 0;
		}
	}


	@media screen and (min-width: 992px) {
		.blob2 {
			top: -60%;
			left: -110%;
			width: 170%;
			height: 100%;
			z-index: 0;
		}
	}

	@media screen and (max-width: 1087px) {
		.Card {
			flex-direction: column;
		}
	}

	@media screen and (min-width: 1200px) {
		.blob2 {
			top: -100%;
			left: -110%;
			width: 170%;
			height: 100%;
			z-index: 0;
		}
	}

	@media screen and (min-width: 1400px) {
		.blob2 {
			top: -120%;
			left: -110%;
			width: 170%;
			height: 100%;
			z-index: 0;
		}
	}

	@media screen and (max-width: 1087px) {
		.CardsContainer {
			flex-direction: column;
		}
	}

	@media screen and (max-width: 991px) {
		.blob2 {
			top: -82%;
			left: -40%;
			width: 170%;
			height: 100%;
			z-index: 0;
			/* margin-top: 15rem; */
		}

		@media (min-width: 768px){
			.container{
				max-width: none;
			}
		}

		@media (min-width: 640px){
			.container{
				max-width: none;
			}
		}

		@media (min-width: 1280px){
			.container{
				max-width: none;
			}
		}
	}
</style>
