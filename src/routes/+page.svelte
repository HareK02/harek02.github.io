<script lang="ts">
    import Header from "$lib/Header.svelte";
    import Footer from "$lib/Footer.svelte";
</script>

<svelte:head>
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link href="https://fonts.googleapis.com/css2?family=Space+Grotesk&display=swap" rel="stylesheet" />
</svelte:head>

<div class="container">
    <section class="hero">
        <div class="scrolldown">
            <img src="images/scroll-down.svg" alt="Scroll down" />
        </div>
    </section>
    <section class="content"></section>
</div>

<style lang="scss">
    :global(body) {
        background-color: #555;
        padding: 0;
        margin: 0;
        font-family: "Space Grotesk", sans-serif;
    }
    .container {
        height: 100lvh;
        overflow-y: scroll;
        overflow-x: hidden;
        scroll-snap-type: y mandatory;
        box-sizing: border-box;
    }
    .hero {
        scroll-snap-align: start;
        padding: 2rem;
        height: 100lvh;
        width: 100vw;
        color: white;
        background-image: url("images/hero.png");
        display: flex;
        flex-direction: row;
        align-items: center;
        box-sizing: border-box;
        .scrolldown {
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            animation: bounce 2s infinite;
            @keyframes bounce {
                0% {
                    transform: translateX(-50%) translateY(0);
                }
                50% {
                    transform: translateX(-50%) translateY(1rem);
                }
                100% {
                    transform: translateX(-50%) translateY(0);
                }
            }
        }
    }
    .content {
        scroll-snap-align: start;
        height: 100lvh;
        width: 100vw;
        padding: 1rem;
        h2 {
            font-size: 2rem;
        }
    }
    @media (min-aspect-ratio: 1/2) {
        .hero {
            flex-direction: column;
            img {
                width: 100%;
                height: auto;
            }
            h1 {
                writing-mode: horizontal-tb;
                font-size: 2rem;
            }
        }
    }
    @media (max-aspect-ratio: 2/1) {
    }
</style>
