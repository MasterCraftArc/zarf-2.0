<script>
    import card from '../assets/png/zarf-card.png';
    export let img;
    export let text;
    export let heroText;
</script>

<div class="container">
    <div class="flex">
        <img class="card" src="{card}" alt="">
        <div class="smallContainer">
            <img class="cardImg" src="{img}" alt="">
            <h1>{heroText}</h1>
            <p>{text}</p>
        </div>
    </div>
</div>

<style>
    .container {
        width: 320px;
        height: 400px;
        display: flex;
        align-items: center;
        justify-content: center;
    }

    .flex {
        display: flex;
        align-items: center;
        justify-content: center;
        padding: 27px;
        width: 320px;
        height: 400px;
    }

    .card {
        z-index: 0;
        width: 300px;
        height: 350px;
        border-radius: 5%;
    }

    .smallContainer {
        width: 320px;
        height: 400px;
        position: absolute;
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
        padding: 37px;
        text-align: center;

    }

    p{
        font-size: 1em;
        font-family: "Roboto";
        color: #FFFF;
        margin-top: .7em;
        font-size: 16px;
    }

    h1 {
        display: flex;
        align-self: center;
        justify-content: center;
        align-items: center;
        font-size: 21px;
        font-family: 'M PLUS Rounded 1c',Tahoma, sans-serif;
    }

    .cardImg {

        width: 100px;
    }

</style>
