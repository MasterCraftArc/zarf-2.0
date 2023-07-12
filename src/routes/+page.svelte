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
	import Spacing from '../components/Spacing.svelte';
	import Defense from '../components/Defense.svelte';
	import AirplaneMode from '../components/AirplaneMode.svelte';
	import { onMount } from 'svelte';

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

		<div class="Card" class:mobileLayout={!isMobile}>
			<Card img={webSecure} heroText='Securely Package Apps & Resources'
				text="Provides the ability to package a chunk of the internet and then securely deliver all of the files and dependencies needed to run an application in a disconnected environment." />

			<Card img={wireLessCloud} heroText='Deploy Cloud Apps While Disconnected'
				text='Provides the ability to deploy apps declaratively and without internet connectivity. Opening up the door for modern cloud capabilities to be deployed in disconnected environments.' />

			<Card img={server} heroText='Easily Maintain Apps While Disconnected'
				text='Zarf reduces the skill and resources needed to manage and update applications in disconnected environments, ensuring no downtime or data loss when updating software.' />
		</div>
	</div>

	<div class="blob2"><AirplaneMode /></div>

	<Columns HeroText='Sometimes Disconnected'
		text='Some systems experience disconnection occasionally due to temporary loss of access, like a rocket going around the moon. Zarf keeps those systems running.' img={rocket} />

	<Column HeroText='Sometimes Disconnected'
		text='Some systems experience disconnection occasionally due to temporary loss of access, like a rocket going around the moon. Zarf keeps those systems running.' img={sub} />

	<Columns HeroText='Disconnected in Emergencies'
		text="The world\'s most important infrastructure needs to be able to control their connection to the internet and still run in the case of internet loss or a cyber attack." img={nuclear} />

	<div class="CardsContainer">
		<div class="Cards">
			<Cards img={community} heroText='Free and Open Source Solution'
				text="Source code is open and viewable to the public which increases security through transparency. Zarf is also a free tool and available for public use." />

			<Cards img={document} heroText='Installs Packages with Two Commands'
				text="Reduces the risk of installation error and complexity of installation procedures by simplifying the installation of packages to just two steps." />
		</div>

		<div class="Cards">
			<Cards img={hosting} heroText='Built to Be Distro Agnostic'
				text="Currently offers fully automated support for K3s, K3d, and Kind. Is also compatible with EKS, AKS, GKE, RKE2 and many others distro services." />

			<Cards img={hosting} heroText='Consistently Deploy Across Environments'
				text="Ensures that applications are deployed the same way each time, whether deployed to a different cluster, machine, or environment." />
		</div>

		<div class="Cards">
			<Cards img={pieces} heroText='Host Registry & Git Server'
				text="Automatically generates an SBOM from the images listed within a package, in compliance with federal mandate. Includes a UI for SBOM viewing." />

			<Cards img={server} heroText='Host Registry & Git Server'
				text="Zarf spins up K8 clusters, docker registries, and git servers offline to allow for disconnected use. For connected users, this provides a failover solution." />
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
		margin: 1em;
	}

	.Card {
		display: flex;
		align-items: flex-start;
		justify-content: flex-start;
	}

	.CardsContainer {
		display: flex;
		flex-wrap: wrap;
		justify-content: center;
		align-items: center;
		text-align: center;
	}

	.cardHolder {
		margin-top: 65em;
		text-align: center;
		display: flex;
		align-items: center;
		justify-content: center;
	}

	.Cards {
		display: flex;
		flex-wrap: wrap;
		justify-content: center;
		align-items: center;
		margin: 10px; /* Add margin for spacing between cards */
		flex-basis: 300px; /* Set the initial width of each card */
		max-width: 400px; /* Set the maximum width of each card */
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
		}
	}
</style>
