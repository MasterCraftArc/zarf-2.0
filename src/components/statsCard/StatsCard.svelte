<script>
    import StatsCard from '../../assets/png/stats-card.png'
    import zarf from '../../assets/png/bigLeapFrog.png'
    import SmallStats from '../../assets/png/stats-card-sm.png'
    import { browser } from '$app/environment';
    import { onMount } from 'svelte';

    let windowWidth

    if (browser){
        windowWidth = window.innerWidth;
    }

    onMount(() => {
        window.addEventListener('resize', () => {
            windowWidth = window.innerWidth;
        });
    });

    const breakpoint = 1147
</script>

<div class="container">
    <div class="text-container">
        <h6>OPEN SOURCE PROJECT</h6>
        <h1>Join our Mission</h1>
        <div class="p">
            <p>Zarf makes modern software capabilities a reality in disconnected environments. We aim to deliver secure software to the world's most important environments.</p>
        </div>
    </div>
<div class="other">
    <div class="small">
        <h1>118</h1>
        <h6>stars</h6>
    </div>
    <div class="small">
        <h1>99</h1>
        <h6>pull requests</h6>
    </div>
<div class="something">
    <div class="small">
        <h1>6</h1>
        <h6>Contributors</h6>
    </div>

    <img src="{zarf}" alt="" class="zarf-image">
</div>
</div>
{#if windowWidth <= breakpoint}
  <img src="{SmallStats}" alt="" class="stats-card">
{:else}
  <img src="{StatsCard}" alt="" class="stats-card">
{/if}

</div>



<style>
.container {
    position: relative;
    display: flex;
    align-items: center;
    justify-content: center;
    z-index: 1;
    margin-top: 5rem;
    margin-bottom: 5rem;
    overflow: hidden;
    margin-left: auto;
    margin-right: auto;
    max-width: 1000px;
}

.other {
    position: absolute;
    top: 2rem;
    right: 2rem;
    display: flex;
    flex-direction: row;
    align-items: center;
    z-index: 2;
    padding: 10px;
}

.something {
    position: absolute;
    top: 12rem;
    display: flex;
    align-items: center;
    z-index: 2;
}

.small {
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 10px;
}

.stats-card {
    position: relative;
    z-index: 1;
    height: 55vh;
    left: 0;
    right: 0;
    margin: auto;
}

h1 {
    padding-bottom: 10px;
    font-size: 60px;
    font-family: 'M PLUS Rounded 1c',Tahoma, sans-serif;
}

.p {
    word-wrap: break-word;
    white-space: normal;
    max-width: 350px;
}

p {
    font-size: 16px;
    color: white;
    max-width: 300px;
}

h6 {
    font-size: 20px;
}

.text-container {
    position: absolute;
    top: 2rem;
    left: 3rem;
    display: flex;
    flex-direction: column;
    align-items: center;
    z-index: 2;
}

.zarf-image {
    height: 200px;
    width: 200px;
    z-index: 1;
}

@media (max-width: 1147px) {
    .container {
      flex-direction: column;
      align-items: center;
      text-align: center;
      justify-content: space-between;
      position: relative;
    }

    h1{
        max-width: 250px;
    }

    .other,
    .something,
    .text-container {
      position: absolute;
      left: 50%;
      transform: translateX(-50%);
    }

    .something,.other {
        right: 15rem;
      bottom: -13rem;

      margin-right: 0;
    }


    .text-container {
      bottom: -66rem;
    }

    .stats-card {
      height: 110vh;
      max-width: 60vw;
    }

    .other{
        flex-direction: column;
        top: 38%;
    }

    .something{
        top: -20%;
        display: flex;
        align-items: center;
        justify-content: center;
    }

    @media (min-width: 1280px){
        .container {
            max-width: none;
        }}

    @media (max-width: 500px){
        .other {
            top: 48%;
        }
        h6{
            min-width: 200px;
        }
        h1{
            font-size: 50px;
        }
        p{
            max-width: 180px;
        }
    }
  }
</style>
