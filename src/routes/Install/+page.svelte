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
    .container{
        margin-bottom: 60rem;
        gap: 100px;
    }

    .blob {
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        width: 150%;
        height: auto;
        z-index: 0;
    }

    .content {
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        text-align: center;
        z-index: 1;
        width: 80%;
        color: white;
    }

    .Copy {
        border: 2px solid #7BD5F4;
        background-color: #2F3459;
        border-radius: 2%;
        height: 45px;
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 0px 10px;
        margin-top: 20px;
        width: 100%;
        box-sizing: border-box;
    }

    button {
        background-color: #2F3459;
        border: none;
        color: white;
    }

    button:hover {
        color: #7BD5F4;
    }

    input {
        background-color: #2F3459;
        border: none;
        color: white;
        width: 100%;
    }

    h1 {
        margin: 0;
    }

    p {
        margin: 10px 0;
    }

    @media (max-width: 768px) {
        .content {
            margin-top: 0;
            width: 100%;
        }
    }

</style>
