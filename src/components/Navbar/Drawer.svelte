<script>
  import { onMount } from 'svelte';
  import hamburger from '../../assets/png/hamburger_menu-removebg-preview.png';

  let hidden = true;

  function toggleMenu() {
    hidden = !hidden;
  }
</script>

<button on:click={toggleMenu}><img src={hamburger} alt=""></button>

{#if !hidden}
<div class="overlay" on:click={toggleMenu}></div>
<div class="menu">
  <button class="close-button" on:click={toggleMenu}><h1>X</h1></button>
  <div class="items">
    <div class="mylinks"><a href="/" >somewhere soon</a></div>
    <div class="mylinks"><a href="/" >somewhere soon</a></div>
    <div class="mylinks"><a href="/" >somewhere soon</a></div>
  </div>

</div>
{/if}

<style>
  img {
    height: 30px;
  }

  .overlay {
    position: fixed;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.5);
    z-index: 999;
  }

  .items{
    display: flex;
    justify-content: center;
    flex-direction: column;
    align-items: center;

  }

  .menu {
    position: fixed;
    left: 0;
    top: 0;
    width: 300px;
    z-index: 1000;
    box-sizing: border-box;
    background-color: #0c143c;
    padding: 20px;
    height: 100vh;
  }

  .close-button {
    margin-bottom: 10px;
  }

  h1{
    font-size: 25px;
    color: #97d358;
  }

  a {
  border: none;
  color: white;
  text-decoration: none;
  justify-content: space-between;
  font-family: 'Roboto';
  font-size: 20px;
  position: relative; /* Add this to make the ::before pseudo-element relative to the link */
}

a:hover{
  color: #97d358;
}

a::before {
  content: '';
  position: absolute;
  left: 0;
  bottom: -2px; /* Move it just below the link text */
  height: 2px;
  width: 100%;
  background-color: #97d358;
  transform: scaleX(0);
  transform-origin: right; /* Start the scaling from the right edge */
  transition: transform 0.3s ease-in-out;
}

a:hover::before {
  transform: scaleX(1); /* Scale the pseudo-element on hover */
  transform-origin: left; /* Scale from the left edge on hover */
}

.mylinks{
  margin: 30px;
}

button{
  padding-left: 25px;
}
</style>
