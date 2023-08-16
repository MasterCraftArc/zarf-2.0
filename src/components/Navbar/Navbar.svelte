<script>
    import github from '../../assets/png/github.png';
    const githubLink = 'https://github.com/defenseunicorns/leapfrogai';
    import slack from '../../assets/svg/slack.svg';
    import leapFrog from '../../assets/png/leapfrog2.png'
    import { onMount } from 'svelte';

    let scrolled = false;
    let currentPage;

    onMount(() => {
        window.addEventListener('scroll', handleScroll);
    });

    function handleScroll() {
        scrolled = window.scrollY > 0;
    };

    onMount (() => {
        currentPage = window.location.pathname
    });


</script>

<div class="navbar" class:scrolled>
    <div class="container">
        <div class="holder">
            <a href="/">
                <img class="leapfrog" src="{leapFrog}" alt="">
            </a>
        </div>

        <div class="links">
            <div class="mylinks">
                <a href="/" class:selected={currentPage === '/'}>PRODUCT</a>
            </div>
            <div class="mylinks">
                <a href="/">EXAMPLES</a>
            </div>
                <div class="mylinks">
                <a href="/">DOCS</a>
            </div>

            <a href="/"><img class="github" src="{slack}" alt=""></a>
            <a href={githubLink}><img class="github" src="{github}" alt=""></a>
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
        display: flex;
        top: 0;
        left: 0;
        width: 100vw;
        z-index: 2;
    }

    .github {
        max-width: 25px;
        background-blend-mode: darken, luminosity;
    }

    .holder {
        display: flex;
        justify-content: space-between;
        margin-left: 1%;
        height: auto;
        width: auto;
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
    }

    .mylinks {
        position: relative;
    }

    .mylinks::after {
        content: '';
        position: absolute;
        left: 0;
        bottom: 0;
        height: 2px;
        width: 100%;
        background-color: #97d358;
        transform: scaleX(0);
        transition: transform 0.3s ease-in-out;
    }



    a {
        margin: 15px;
        border: none;
        color: white;
        text-decoration: none;
        justify-content: space-between;
        font-family: 'Roboto';
        font-size: 14px;
    }

    .selected {
        border-bottom: 2px solid #97d358;
        color: #97d358;
    }

    .links {
        display: flex;
        align-items: center;
        justify-content: flex-end;
    }

    a:hover::after {
        transform: scaleX(1);
    }
</style>
