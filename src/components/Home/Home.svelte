<script>
    import zarfEdge from '../../assets/png/zarf-edge.png';
    import { onMount } from 'svelte';

    let initialData;

    onMount(async () => {
        const res = await fetch('/Install');
        initialData = await res.json();
    });
</script>

<div class="Container">
    <div class="FlexContainer">
        <div class="left">
            <h1>DevSecOps for Airgap</h1>
            <p>A free open source tool that enables continuous software delivery on disconnected networks.</p>
            <button><a  href="/Install">Install Now</a></button>
        </div>
        <div class="right">
            <img class="zarfEdge" src="{zarfEdge}" alt="">
        </div>
    </div>
</div>


<style>

.Container{
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    padding: 10px;
    width: 100%;
    height: 25%;
}

.FlexContainer{
    display: flex;
    justify-content: space-evenly;
    align-items: center;
    top:50%;
    left:50%;
}

.right{
    display: flex;
    flex-basis: 50%;
}

.left{
    display: flex;
    flex-basis: 50%;
    flex-direction: column;
    align-items: center;
    justify-content: center;
}

img{
    height: 500px;
}

p {
  font-size: 25px;
  color: white;
  padding-left: 15%;
}

button {
    border-radius: 50px;
    border: none;

    background-color: aqua;
    margin-top: 6%;
    width: 126px;
    height: 36px;
  }
  h1{
    color: white;
    margin-bottom: 15%;
  }

  a, a:hover, a:focus, a:active{
    text-decoration: none;
    color: black;
  }
</style>
