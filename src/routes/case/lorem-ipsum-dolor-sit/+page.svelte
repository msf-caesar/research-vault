<script lang="ts">
    import "$lib/css/global.css";
    import Link from "$lib/components/Link.svelte";
</script>

<svelte:head>
    <title>Case study - Lorem ipsum dolor sit</title>
</svelte:head>

<div class="page-layout">
    <section>
        <h6>Case study</h6>
        <h1>Lorem ipsum dolor sit</h1>
        <hr />
    </section>
    <main>
        {#each Array(5) as _}
            <h4 id="quibusdam">Repellendus quibusdam, odio, sed sapiente!</h4>
            <p>
                Lorem ipsum dolor sit amet consectetur adipisicing elit. Nulla,
                in necessitatibus amet suscipit at, numquam facilis unde odio
                porro dicta eius libero quae, esse soluta consectetur quis
                tempore molestiae quo. Lorem ipsum, dolor sit amet consectetur
                adipisicing elit. Vitae explicabo ab quia pariatur eos unde id
                inventore, soluta provident sint. Amet delectus enim optio
                praesentium deserunt corrupti velit asperiores nihil.
            </p>
            <p>
                Lorem ipsum dolor sit amet consectetur adipisicing elit. Quis
                illo, mollitia ipsa nihil sequi <b>accusantium</b> quam maiores eum
                cupiditate quidem neque eos voluptates itaque provident corrupti
                nesciunt excepturi ut fuga!
            </p>
        {/each}
    </main>
    <footer>
        <div class="sticky-panel">
            <hr class="subtle-divider mobile-styles" />
            <h4>About us</h4>
            <p>
                Lorem ipsum dolor sit, amet consectetur adipisicing elit.
                Fugiat, obcaecati consequuntur.
            </p>
            <h4>Founded</h4>
            <p>Lorem city, 2020</p>
            <hr class="subtle-divider" />
            <h4>Next case study</h4>
            <p>
                <Link href="/" external>Consectetur adipisicing</Link>
            </p>
        </div>
    </footer>
</div>

<style>
    /* Define styles for the page layout */
    .page-layout {
        padding: 0 20px;
        max-width: 1100px;
        margin: 80px auto;
        /* Set grid display with a gap */
        gap: 0 80px;
        display: grid;
    }

    /* Styles for paragraphs */
    p {
        padding: 20px 0;
        line-height: 1.5;
    }

    /* Styles for heading level 1 */
    h1 {
        font-family: "Zirlo", serif;
        font-size: 2rem;
    }

    /* Styles for heading level 4 */
    h4 {
        padding-top: 20px;
        font-family: "Zirlo", serif;
        font-size: 1.1rem;
    }

    /* Styles for heading level 6 (Subtitle) */
    h6 {
        font-family: "Zirlo", serif;
        font-size: 1rem;
        /* Add gradient background to subtitle text */
        color: transparent;
        background-clip: text;
        background-image: linear-gradient(to bottom left, #0b68cb, #113264);
    }

    /* Styles for horizontal rule (divider) */
    hr {
        border: none;
        border-top: solid 1px #dddde4;
        margin-top: 40px;
    }

    /* Styles for a subtle divider */
    hr.subtle-divider {
        width: 40px;
        margin-bottom: 40px;
    }

    /* Media query for screens with a minimum width of 880px */
    @media only screen and (min-width: 880px) {
        /* Reset styles for .mobile-styles class */
        .mobile-styles {
            all: unset;
        }
        /* Define grid layout for larger screens */
        .page-layout {
            grid-template-columns: 1fr 400px;
        }
        /* Make .sticky-panel sticky */
        .sticky-panel {
            top: 40px;
            position: sticky;
        }
        /* Position section element in the grid */
        section {
            grid-column: 1 / 2;
            grid-row: 1 / 2;
        }
        /* Position main element in the grid */
        main {
            grid-column: 1 / 2;
            grid-row: 2 / 3;
        }
        /* Position footer element in the grid */
        footer {
            grid-column: 2 / 3;
            grid-row: 2 / 3;
            position: relative;
        }
        /* Add scroll padding to body and html elements */
        :global(body, html) {
            scroll-padding-top: 40px;
        }
    }
</style>
