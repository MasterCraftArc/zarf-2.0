<script>
    import github from '../../assets/png/github.png';
    const githubLink = 'https://github.com/defenseunicorns/zarf';
    import slack from '../../assets/svg/slack.svg';
    import { onMount } from 'svelte';
    import Drawer from './Drawer.svelte';
    import leapFrog from '../../assets/png/leapfrog2.png'

    let scrolled = false;

    onMount(() => {
        window.addEventListener('scroll', handleScroll);
    })

    function handleScroll () {
        scrolled = window.scrollY > 0
    }

</script>

<div class="navbar" class:scrolled>
    <div class="container">
        <slot><Drawer/></slot>

        <div class="holder">
            <a href="/">
                <img class="leapfrog" src="{leapFrog}" alt="">
            </a>
        </div>

        <div class="links">
            <a href={githubLink}><img class="github" src="{github}" alt=""></a>
            <a href="/"><img class="github" src="{slack}" alt=""></a>
        </div>
    </div>

</div>

<style>

.scrolled {
    background-color: #0c143c;
    transition: background-color .5s ease-in-out;
    box-shadow: 0 2px 4px 0 rgba(0,0,0,.5);
  }

    .navbar {
        position: fixed;
        top:0;
        left: 0;
        width: 100vw;
        z-index: 2;
    }

    .github {
        max-width: 30px;
        background-blend-mode: darken, luminosity;
    }

    .holder {
        display: flex;
        justify-content: space-between;
        margin-left: 1%;
    }

    .leapfrog {
        height: auto;
        width: 200px;
        display: flex;
        justify-content: space-between;
        align-items: center;
    }

    .container {
        display: flex;
        justify-content: space-between;
        align-items: center;
        width: 100%;
        height: 80px;
        z-index: 0;

        max-width: none;
        padding: 1em;
    }

    a {
        margin: 5px;
        border: none;
        color: white;
        text-decoration: none;
        justify-content: space-between;
    }

    .links {
        display: flex;
        justify-content: space-evenly;
        align-items: center;
        margin-right: 2%;
        padding: 25px;
    }

</style>
