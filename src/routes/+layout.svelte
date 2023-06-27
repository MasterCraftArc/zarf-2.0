<script>
  import Navbar from "../components/Navbar/Navbar.svelte";
  import { onMount } from "svelte";

  onMount(() => {
    const link = document.createElement("link");
    link.href = "https://fonts.googleapis.com/css2?family=Roboto&display=swap";
    link.rel = "stylesheet";
    document.head.appendChild(link);
  });
</script>

<style>
  :root {
    background-color: #0c143c;
    margin: 0;
    padding: 0;
    font-family: 'Roboto', sans-serif; /* Use 'Roboto' font family */
  }
</style>

<Navbar />
<!-- <footer><Footer/></footer> -->
<slot />
