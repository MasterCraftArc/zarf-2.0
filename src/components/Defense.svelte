<script>
	import Blob from "./blob/Blob.svelte";
	import Doug from "../assets/png/full-du-logo.png";
</script>

<div class="blob-container">

	<div class="text-container">
		<h1>Created & Maintained by:</h1>
		<img src="{Doug}" alt="" class="image-on-blob">
		<p>For enterprise package support information</p>
		<button>CONTACT A EXPERT</button>
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
	margin-top: 10rem;
	margin-bottom: 15rem;
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
}

.text-container h1, .text-container p {
	margin: 0;
}

.image-on-blob {
	max-width: 80%;
	max-height: 80%;
	margin-top: 20px;
}

.blob{
    width: 200%;
}
button {
    border-radius: 50px;
    border: none;
    background-color: #787FF5;
    margin-top: 6%;
    width: 176px;
    height: 36px;
	color: white
}

h1{
	font-size: 24px;
	font-family: "M PLUS rounded 1c";
}
</style>
