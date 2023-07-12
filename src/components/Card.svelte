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
        padding: 27px;
        margin: 2em;
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
        width: 200%;
        height: 120%;
    }

    .smallContainer {
        width: 265px;
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
    }

    h1 {
        display: flex;
        align-self: center;
        justify-content: center;
        align-items: center;
        font-size: 21px;
    }

    .cardImg {
        height: 100px;
        width: 100px;
    }

    img {
        height: 400px;
        width: 320px;
    }

</style>
