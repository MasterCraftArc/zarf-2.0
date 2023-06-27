<script>
    import github from '../../assets/png/github.png';
    const githubLink = 'https://github.com/defenseunicorns/zarf';
    import slack from '../../assets/svg/slack.svg';
    import zarf from '../../assets/png/zarf-logo.png';
</script>

<div class="navbar">
    <div class="container">
        <div class="holder">
            <a href="/">
                <img class="zarf" src="{zarf}" alt="">
            </a>
        </div>

        <div class="links">
            <a href="/">PRODUCT</a>
            <a href="/">EXAMPLES</a>
            <a href="/">DOCS</a>
            <a href={githubLink}><img class="github" src="{github}" alt=""></a>
            <a href="/"><img class="github" src="{slack}" alt=""></a>
        </div>
    </div>
</div>

<style>

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
