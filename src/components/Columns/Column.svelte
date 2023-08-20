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

    }


    .right {
        width: 30%;
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
        font-family: 'M PLUS Rounded 1c',Tahoma, sans-serif;
    }

    p{
        font-family: "Roboto";
    }

    @media screen and (max-width: 991px) {
        .container {
            flex-direction: column;
            margin-top: 5rem;
        }

        .left,
        .right {
            width: 100%;
        }

        .left{
            display: flex;
            align-items: center;
            justify-content: center;
        }
    }
</style>
