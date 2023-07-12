<script>
    export let img;
    export let text;
    export let heroText
</script>

<div class="container">
    <div class="flex">
        <div class="smallContainer">
            <img class="cardImg" src={img} alt="">
            <h1>{heroText}</h1>
            <p>{text}</p>
        </div>
    </div>
</div>

<style>
    .container {
        margin-top: 5%;
    }

    .flex {
        display: flex;
        align-items: center;
        justify-content: center;
        flex-direction: column;
        flex-wrap: wrap;
    }

    .smallContainer {
        height: 450px;
        width: 200px;
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
        /* padding: 27px 24px 27px 24px; */
        margin: 1em;
        flex-wrap: wrap;
        box-sizing: border-box; /* Include padding and borders in width and height calculations */
    }

    .cardImg {
        height: 85px;
    }

    h1 {
        display: flex;
        align-self: center;
        justify-content: center;
        align-items: center;
        font-size: 24px;
    }

    p{
        font-size: 16px;
    }
</style>
