<script>
    import StatsCard from '../../assets/png/stats-card.png'
    import zarf from '../../assets/png/zarf-bubbles.png'
</script>

<div class="container">
    <div class="text-container">
        <h6>OPEN SOURCE PROJECT</h6>
        <h1>Join our Mission</h1>
        <div class="p">
            <p>Zarf makes modern software capabilities a reality in disconnected environments. We aim to deliver secure software to the world's most important environments.</p>
        </div>
    </div>
    <img src="{StatsCard}" alt="" class="stats-card">
    <img src="{zarf}" alt="" class="zarf-image">
</div>


<style>
.container {
    position: relative;
    display: flex;
    align-items: center; /* Align items to the top */
    justify-content: center; /* Justify content to the left */
    z-index: 1;
    max-width: 100%; /* Set maximum width to 100% */
    overflow: hidden; /* Hide the overflow content */

}

.stats-card {
    height: 45vh;
    width: 90vw;
    z-index: 1;
}

h1 {
    padding-bottom: 10px;
    font-size: 60px;
    margin-left: 2rem;
}

.p {
    width: 75%;
    margin-left: 2rem;
    word-wrap: break-word; /* Breaks long words */
    white-space: normal; /* Wraps text within the container */
}

p {
    font-size: 16px;
}

h6 {
    font-size: 20px;
    margin-left: 2rem;
}

.text-container {
    position: absolute;
    top: 0;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: flex-start;
    padding: 0 1%;
    z-index: 2;
    margin-top: 2rem;
    max-width: 100%; /* Set maximum width to 100% of the container */
}

.zarf-image {
    position: absolute;
    bottom: 0;
    right: -1;
    height: 200px;
    width: 200px;
    z-index: 1;
}

@media (max-width: 992px) {
    .stats-card {
        height: 110vh;
        width: 60vw;
    }

    .text-container{
        width: 300px;
    }
}
</style>
