<script>
	import Blob from "./blob/Blob.svelte";
</script>

<div class="blob-container">

	<div class="text-container">
		<h1>Airplane Mode for the Cloud</h1>
		<h6>Modern software assumes your systems have access to the internet. This may work for 99% of the world, but certain SECURE systems need to maintain capabilities while being disconnected from the internet. Zarf keeps your software running, no matter your connection status.</h6>
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
	top: 50%;
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
</style>
