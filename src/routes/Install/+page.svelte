<script>
    import Blob from "../../components/blob/Blob.svelte";
    import { copy } from 'svelte-copy';
    import C from "../../components/Install/Install.svelte";

    let textToCopy = "brew tap defenseunicorns/tap && brew install zarf";


</script>



<div class="container">
    <div class="blob"><Blob/></div>
    <div class="content">
        <h1>INSTALL ZARF</h1>
        <p>On macOS or Linux, you can easily install Zarf in your terminal by using Brew.</p>
        <div class="Copy">
            <input type="text" bind:value="{textToCopy}" readonly/>
            <button use:copy={textToCopy}>
                copy
            </button>
        </div>
        <p>For more detailed installation instructions - check out our Getting Started Doc.</p>
    </div>
</div>
<C/>

<style>
    .blob {
        z-index: 0;
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        height: 100%;
        width: 100%;

    }

    .container {
        display: flex;
        align-items: center;
        justify-content: center;
        height: 100%;
        width: 100%;
        margin-bottom: 55%;
    }

    .content {
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        text-align: center;
    }

    .Copy{
        border: #7BD5F4;
        border-style: solid;
        border-width: 2px;
        background-color: #2F3459;
        border-radius: 2%;
        height: 45px;
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding:  0px 10px 0px 10px;
    }
    button{
        background-color: #2F3459;
        border: none;
        color:white
    }
    button:hover{
        color:#7BD5F4
    }
    input{
        background-color: #2F3459;
        border: none;
        color:white;
        width: 100%;
    }

    h1{
        color: white;
    }

    p{
        color:white
    }
</style>
