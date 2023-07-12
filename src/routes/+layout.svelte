<script>
	import '../app.postcss';
	import Navbar from '../components/Navbar/Navbar.svelte';
	import MobileNav from '../components/Navbar/MobileNav.svelte';
	import { onMount } from 'svelte';

	let isMobile

	onMount(() => {
		const link = document.createElement('link');
		link.href = 'https://fonts.googleapis.com/css2?family=Roboto&display=swap';
		link.rel = 'stylesheet';
		document.head.appendChild(link);
	});

	onMount(() => {
	window.addEventListener('resize',handleResize)
	handleResize()
	})

	function handleResize(){
		isMobile = window.innerWidth <= 992;

	}
</script>

{#if !isMobile}
<Navbar />
{:else}
<MobileNav />
{/if}

<slot />

<style>
	:root {
		background-color: #0c143c;
		margin: 0;
		padding: 0;
		font-family: 'Roboto', sans-serif; /* Use 'Roboto' font family */
		box-sizing: 0;
	}
	* {
		margin: 0;
		padding: 0;
	}
</style>
