<script>
	import Blob from "./blob/Blob.svelte";
</script>

<div class="blob-container">

	<div class="text-container">
		<h1>Generative AI for Disconnected Systems</h1>
		<h6>Modern Generative AI assumes your systems have access to the internet. This may work for 99% of the world, but certain SECURE systems need to maintain capabilities while being disconnected from the internet. LeapfrogAI provides the advanced AI capabilities available on the open internet in your Airgapped system</h6>
	</div>
</div>

<style>
.blob-container {
	position: relative;
	width: 100%;
	height: 100vh;
	display: flex;
	align-items: center;
	justify-content: center;
	margin-top: 15rem;
	margin-bottom: 12rem;
}

.blob-container {
	width: 100%;
	height: 100%;

}

.text-container {
	position: absolute;
	/* top: 0%; */
	margin-top: 9rem;
	left: 50%;
	transform: translate(-50%, -50%);
	text-align: center;
	z-index: 1;
	padding: 20px;
	box-sizing: border-box;
}

.text-container h1{
	margin: 0;
}



.text-container h1 {
	margin-bottom: 10px;
}

h1{
	font-size: 48px;
}

h6{
	font-size: 20px;
}

@media screen and (max-width: 991px) {
	.text-container{
		margin-bottom: 15rem;
		margin-top: 35rem;
	}
	.blob-container{
		margin-top: 25rem;
	}
}
</style>
