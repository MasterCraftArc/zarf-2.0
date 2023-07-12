<script>
    import github from '../../assets/png/github.png';
    const githubLink = 'https://github.com/defenseunicorns/zarf';
    import slack from '../../assets/svg/slack.svg';
    import zarf from '../../assets/png/zarf-logo.png';
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
                <img class="zarf" src="{zarf}" alt="">
            </a>
        </div>

        <div class="links">
            <a href="/" class:selected={currentPage === '/'}>PRODUCT</a>
            <a href="/">EXAMPLES</a>
            <a href="/">DOCS</a>
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
}

.zarf {
    height: 50px;
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
    overflow: hidden;
    max-width: none;
    padding: 1em;
}

.selected{
    border-bottom: 2px solid turquoise;
    color: turquoise;
}

a {
    margin: 5px;
    border: none;
    color: white;
    text-decoration: none;
    justify-content: space-between;
}

a:hover {
    border-bottom: 2px solid turquoise;
    color: turquoise;
}

a:hover::after {
    transform: scaleX(1);
}



.links {
    display: flex;
    align-items: center;
    justify-content: flex-end;
}
</style>
