<script>
    import zarfEdge from '../../assets/png/zarf-edge.png';
    import { onMount } from 'svelte';
    import bigLeapFrog from '../../assets/png/bigLeapFrog.png'

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
                <a href="/Install"><button>INSTALL NOW</button></a>
            </div>
        </div>
        <div class="right">
            <img class="bigLeapFrog" src="{bigLeapFrog}" alt="">
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
            margin-right: 5%;
            margin-top: 5em;
            position: absolute;
            padding-left: 32px;
            overflow: hidden;
        }

        .left {
            display: flex;
            flex-direction: column;
            justify-content: flex-start;
            align-items: flex-start;
            position: relative;
            width: 100%;
            overflow: hidden;
            margin-left: 2rem;
        }

        .content {
            display: flex;
            align-items: flex-start;
            justify-content: flex-start;
            flex-direction: column;
            align-content: center;
            margin-left: 20px;
        }

        p {
            font-size: 46px;
            letter-spacing: -0.25px;
            font-weight: 400;
            line-height: 1.167;
            color: white;
            padding-bottom: 25px;
            white-space: normal;
            word-wrap: break-word;
        }

        h6 {
            font-size: 20px;
            color: white;
            max-width: 50%;
            text-align: left;
            margin: 0;
            color: #BEBFC9;
            font-family: 'Roboto';
        }

        button {
            border-radius: 50px;
            border: none;
            background-color:#97d358 ;
            margin-top: 15%;
            width: 145px;
            height: 42px;
            font-size: 15px;
            font-family: 'Roboto';
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
            overflow: hidden;
        }

        .right img {
            height: 360px;
            width: auto;
            flex-shrink: 0;
        }

        @media screen and (min-width: 1072px) {


            .FlexContainer {
                flex-direction: row;
                margin-left: 2rem;
                margin-top: .2em;
            }

            p {
                font-size: 96px;
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
                height: 450px;
                width: auto;

            }
        }

    </style>
