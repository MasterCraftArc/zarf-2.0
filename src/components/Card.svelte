<script>
    import card from '../assets/png/zarf-card.png'
    export let img;
    export let text;
    export let heroText
</script>

<div class="container">
    <div class="flex">
        <img class="card" src="{card}" alt="">
        <div class="smallContainer">
            <img class="cardImg" src={img} alt="">
            <h1>{heroText}</h1>
            <p>{text}</p>
        </div>
    </div>
</div>

<style>
    .container {
        position: relative;
        display: flex;
        align-items: center;
        justify-content: center;
        margin-top: 100%;
    }

    .flex {
        display: flex;
        align-items: center;
        justify-content: center;
        flex-direction: column;
    }

    .card {
        z-index: -1;
    }

    .smallContainer {
        position: absolute;
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
        padding: 27px 24px 27px 24px;
        overflow: hidden;
        flex-wrap: wrap; /* Add flex-wrap: wrap to allow cards to wrap */
    }

    .cardImg {
        height: 85px;
    }

    h1 {
        display: flex;
        align-self: center;
        justify-content: center;
        align-items: center;
        color: white;
    }

    p {
        color: white;
    }
</style>
