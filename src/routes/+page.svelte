<script>
    import Landing from "../lib/landing.svelte";
    // import Welcome from "../lib/welcome.svelte";
    // import Carousel from "$lib/components/carousel.svelte";
    // import Resume from "$lib/resume.svelte";
    // import Gallery from "$lib/gallery.svelte";
</script>

<main>
    <Landing />
    <!-- <Welcome />
    <div id="carousel-wrapper">
        <Carousel />
    </div>
    <Resume />
    <Gallery /> -->
</main>


<style>    
    :root {
        --background-color: #fdf0e6;
        --secondary-background-color: #e6f3fd;
        --tertiary-background-color: white;
        --primary-red: rgb(240, 142, 128);
    }

    main {
        background-color: var(--background-color);

        font-family: 'Montserrat', sans-serif;
        font-family: 'Open Sans', sans-serif;
        font-size: 1rem;

        line-height: 1.7rem;
        letter-spacing: .05rem;
        word-spacing: .05rem;

        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
    }

    #carousel-wrapper {
        margin: 2rem;
        padding: 4rem 2rem;
        background-color: var(--tertiary-background-color);
        border-radius: 10px;
    }
</style>
