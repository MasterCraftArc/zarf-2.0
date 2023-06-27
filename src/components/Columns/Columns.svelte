<script>
export let HeroText
export let text
export let img
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
    .container{
        display: flex;
        justify-content: space-evenly;
        flex-direction: row;
        margin: 10%;
    }
    .left{
        width: 50%;
        display: flex;
        flex-direction: column;
        justify-content: center;
    }
    .right{
        width: 50%;
    }
    img{
        height: 400px;
    }
    h1{
        color: white;
        margin-bottom: 2%;
    }
    p{
        color: white;
    }
</style>
