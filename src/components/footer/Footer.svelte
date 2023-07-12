<script>
    import github from '../../assets/png/github.png'
    const githubLink = 'https://github.com/defenseunicorns/pepr'
    import slack from '../../assets/svg/slack.svg'
    import zarf from '../../assets/png/zarf-footer.png'
</script>

<div class="container">
    <img class="zarf" src="{zarf}" alt="">

    <div class="holder">
        <a href={githubLink}><img class="github" src="{github}" alt=""></a>
        <a href="/"><img class="github" src="{slack}" alt=""></a></div>
        <p>copyright © 2022 Zarf Project. All rights reserved</p>
    </div>


<style>
    .container{
        display: flex;
        flex-direction: column;
        align-items: center;
    }

    .zarf{
        height: 100px;
        width: 100px;
    }

    .github{
        max-width: 25px;
    }
    p{
        margin-bottom: 5%;
        margin-top: 2%;
        color: white;
    }
    .holder{
        padding-top: 2%;
    }
</style>
