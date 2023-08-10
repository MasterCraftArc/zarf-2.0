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
        margin-right: 2rem;
        bottom: 100;
        margin-bottom: 0;
        padding-bottom: 0;
    }

    .zarf{
        height: 100px;
        width: 100px;
        margin-left: 15px;
    }

    .github{
        max-width: 25px;
    }
    p{
        margin-bottom: 5%;
        margin-top: 2%;
        color: white;
    }
    a{
        margin: 5px;
    }
    .holder{
        padding-top: 2%;
        display: flex;
        flex-direction: row;
        justify-content: space-between;
    }
</style>
