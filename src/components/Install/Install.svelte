<script>
    import { copy } from 'svelte-copy';


    let brew = 'brew install kind && kind delete cluster && kind create cluster';

    let zarf = 'zarf  init'

    let zarfPackage = 'zarf package deploy sget://defenseunicorns/zarf-hello-world:$(uname -m)'
</script>

<div class="bigContainer">
    <h1>Try It Now</h1>
    <p>You are ready to deploy code in Airgap copy the following commands to get started</p>
    <div class="CopyContainer">
        <div class="content">
            <div class="Copy">
                <input type="text" bind:value="{brew}" readonly/>
                <button use:copy="{brew}">
                    copy
                </button>
            </div>
        </div>
        <div class="content">
            <div class="Copy">
                <input type="text" bind:value="{zarf}" readonly/>
                <button use:copy="{zarf}">
                    copy
                </button>
            </div>
        </div>
        <div class="content">
            <div class="Copy">
                <input type="text" bind:value="{zarfPackage}" readonly/>
                <button use:copy="{zarfPackage}">
                    copy
                </button>
            </div>
        </div>
    </div>
    <button id="docs">VIEW DOCUMENTATION</button>
</div>

<style>
    .bigContainer {
        margin-top: 175px;
        display: flex;
        align-items: center;
        justify-content: center;
        margin-top: 100%;
        flex-direction: column;
    }

    .CopyContainer {
        display: flex;
        border: 2px solid #7BD5F4;
        background-color: #2F3459;
        border-radius: 2%;
        height: 35vh;
        width: 75vw;
        flex-direction: column;
        align-items: center;
        justify-content: space-evenly;
        padding: 10px;
        flex-shrink: 2;
    }

    .Copy {
        display: flex;
        flex-direction: row; /* Modified to column */
        align-items: center;
        justify-content: space-evenly; /* Added */
        width: 100%;
        margin-top: 20px;
    }

    button {
        background-color: #2F3459;
        border: none;
        color: white;
    }

    #docs{
        margin-top: 2%;
        background-color: #787FF5;
        width: 126px;
        height: 36px;
        border-radius: 50px;
        border: none;
        display: flex;
        justify-content: center;
        align-items: center;
        padding: 5px 5px 5px 5px;

    }

    button:hover {
        color: #7BD5F4;
    }

    input {
        background-color: #2F3459;
        border: none;
        color: white;
        width: 650px;
    }

    img{
        height: 35px;
    }

    h1 {
        color: white;
    }

    p {
        color: white;
    }
</style>
