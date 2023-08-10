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
            <div class="text"><p>{text}</p></div>

        </div>
    </div>
</div>

<style>
    .container {
        margin:0;
    }

    .flex {
        display: flex;
        align-items: center;
        flex-direction: column;
        flex-wrap: wrap;
    }

    .text{
        width: 238px;
        height: 114px;
        text-align: left;
    }

    .smallContainer {
        height: 350px;
        width: 200px;
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
        margin: 15px;
        box-sizing: border-box;
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
        font-family: 'M PLUS Rounded 1c',Tahoma, sans-serif;
        margin-top: 10px;
        margin-bottom: 10px;
    }

    p{
        font-size: 16px;
    }
</style>
