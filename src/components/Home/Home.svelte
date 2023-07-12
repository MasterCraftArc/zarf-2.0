<script>
    import zarfEdge from '../../assets/png/zarf-edge.png';
    import { onMount } from 'svelte';
    import Blob from '../blob/Blob.svelte';

    let initialData;

    onMount(async () => {
        const res = await fetch('/Install');
        initialData = await res.json();
    });
</script>



    <div class="FlexContainer">
        <div class="left">
            <div class="content">
                <p>DevSecOps for Airgap</p>
                <h6>A free open source tool that enables continuous software delivery on disconnected networks.</h6>
                <button><a href="/Install">INSTALL NOW</a></button>
            </div>
        </div>
        <div class="right">
            <img class="zarfEdge" src="{zarfEdge}" alt="">
        </div>
    </div>



    <style>
        .FlexContainer {
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            align-items: center;
            width: 100%;
            min-height: 75vh;
            margin: 5%;
            margin-top: 6em;
            position: absolute;
            padding-left: 5%;
            overflow: hidden; /* Prevent children from overflowing */
        }

        .left {
            display: flex;
            flex-direction: column;
            justify-content: flex-start;
            align-items: flex-start;
            position: relative;
            width: 100%;
            overflow: hidden;
        }

        .content {
            display: flex;
            align-items: flex-start;
            justify-content: flex-start;
            flex-direction: column;
            align-content: center;
            margin-left: 20px; /* Add margin to space content div from the left */
        }

        p {
            font-size: 48px;
            letter-spacing: -0.25px;
            font-weight: 400;
            line-height: 1.167;
            color: white;
            padding-bottom: 25px;
            white-space: normal; /* Reset white-space to allow wrapping */
            word-wrap: break-word; /* Break word if it exceeds container width */
        }

        h6 {
            font-size: 25px;
            color: white;
            max-width: 50%;
            text-align: left;
            margin: 0; /* Remove default margin */
        }

        button {
            border-radius: 50px;
            border: none;
            background-color: aqua;
            margin-top: 6%;
            width: 126px;
            height: 36px;
            font-size: 14px;
            letter-spacing: 0.4px;
        }

        a,
        a:hover,
        a:focus,
        a:active {
            text-decoration: none;
            color: black;
        }

        .right {
            display: flex;
            justify-content: center;
            align-items: center;
            width: 100%;
            margin-top: 50px;
            overflow: hidden; /* Prevent children from overflowing */
        }

        .right img {
            height: 450px;
            width: auto;
        }

        @media screen and (min-width: 1072px) {
            .FlexContainer {
                flex-direction: row;
                margin-left: 2em;
            }

            .left {
                width: 50%;
                align-items: flex-start;
                justify-content: flex-start;
            }

            .content {
                align-items: flex-start;
                justify-content: flex-start;
            }

            .right {
                width: 50%;
            }

            .right img {
                height: 550px;
                width: auto;
            }
        }
    </style>
