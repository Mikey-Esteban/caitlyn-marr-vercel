<script>
    import { onMount } from 'svelte';
    import { fade } from 'svelte/transition';
    import Downarrow from '$lib/components/downarrow.svelte';


    let visible = false;

    function loadContent() {
        visible = true;
    }

    onMount(async() => {
        const video = document.querySelector('#video');
        video.addEventListener('ended', (event) => {
            console.log('video has ended')
            loadContent();
        });
    });
</script>

<main>
    <video
        muted
        autoPlay
        playsinline
        id="video"
    >
        <source src="/assets/videos/caitlyn-marr-clip.mp4" type="video/mp4" />
    </video>
    {#if visible}
        <div id="content" transition:fade>
            <div id="shadow">
                <div class="opaque" id="landingContent">
                  <h1 id="title">CAITLYN MARR</h1>
                  <h3>ACTOR</h3>
                  <!-- <Downarrow /> -->
                  <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" height="24" width="24">
                    <path xmlns="http://www.w3.org/2000/svg" d="M12 4C12.5523 4 13 4.44772 13 5V16.5858L17.2929 12.2929C17.6834 11.9024 18.3166 11.9024 18.7071 12.2929C19.0976 12.6834 19.0976 13.3166 18.7071 13.7071L12.7071 19.7071C12.3166 20.0976 11.6834 20.0976 11.2929 19.7071L5.29289 13.7071C4.90237 13.3166 4.90237 12.6834 5.29289 12.2929C5.68342 11.9024 6.31658 11.9024 6.70711 12.2929L11 16.5858V5C11 4.44772 11.4477 4 12 4Z" fill="#fff"></path>
                    </svg>
                </div>
              </div>
        </div>
    {/if}
</main>

<style>
    main {
        position: relative;
    }

    h1 {
        margin: 1rem;
        font-size: 3rem;
    }

    h3 {
        margin: 1rem;
        font-size: 2rem;
    }

    #video {
        z-index: -10;
        top: 0;
        width: 100vw;
        max-width: 100%;
        height: 100vh;
        background: black;
        display: block;
        outline: none;
    }

    #content {
        position: absolute;
        top: 0;
        color: white;
        width: 100%;
        height: 100vh;
        background-color: rgba(0,0,0,.3);
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
    }
</style>