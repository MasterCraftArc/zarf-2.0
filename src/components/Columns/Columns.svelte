<script>
    export let HeroText;
    export let text;
    export let img;
</script>

<div class="container">
    <div class="left">
        <h1>{HeroText}</h1>
        <p>{text}</p>
    </div>

    <div class="right">
        <img src={img} alt="">
    </div>
</div>

<style>
    .container {
        display: flex;
        justify-content: space-evenly;
        flex-direction: row;
        margin: 2%;
    }

    .left {
        width: 30%;
        display: flex;
        flex-direction: column;
        justify-content: center;
    }


    img {
        max-height: 350px;
        max-width: 350px;
    }

    p{
        font-family: "Roboto";
    }

    .right{
        display: flex;
        justify-content: center;
        align-items: center;
    }

    h1 {
        color: white;
        margin-bottom: 2%;
        font-size: 43px;
        margin-bottom: 25px;
        font-family: 'M PLUS Rounded 1c',Tahoma, sans-serif;
    }

    @media screen and (max-width: 991px) {
        .container {
            flex-direction: column;
        }

        .left,
        .right {
            width: 100%;
        }

        .right {
            order: -1;
            display: flex;
            justify-content: center;
            margin-bottom: 10rem;
        }

        .container{
            text-align: center;
            margin-top: 5rem;
        }
    }
</style>
