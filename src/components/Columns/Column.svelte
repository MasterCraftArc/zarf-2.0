<script>
    export let HeroText;
    export let text;
    export let img;
</script>

<div class="container">
    <div class="left">
        <img src="{img}" alt="">
    </div>

    <div class="right">
        <h1>{HeroText}</h1>
        <p>{text}</p>
    </div>
</div>

<style>
    .container {
        display: flex;
        justify-content: space-evenly;
        flex-direction: row;
        margin: 10%;
    }

    .left {
        width: 50%;
        display: flex;
        flex-direction: column;
        justify-content: center;
    }

    .right {
        width: 50%;
    }

    img {
        max-height: 350px;
        max-width: 350px;
    }

    h1 {
        color: white;
        margin-bottom: 2%;
        font-size: 43px;
        margin-bottom: 25px;
    }



    @media screen and (max-width: 991px) {
        .container {
            flex-direction: column;
        }

        .left,
        .right {
            width: 100%;
        }

        .left{
            display: flex;
            align-items: center;
        }
    }
</style>
