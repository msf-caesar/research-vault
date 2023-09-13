<script lang="ts">
    import "$lib/css/global.css";
    import Link from "$lib/components/Link.svelte";
</script>

<svelte:head>
    <title>
        Case study - Development of a Resource Management System for the Oil
        Industry
    </title>
</svelte:head>

<div class="page-layout">
    <section>
        <h6>Case study</h6>
        <h1>
            Development of a Resource Management System for the Oil Industry
        </h1>
        <hr />
    </section>
    <main>
        {#each Array(10) as _}
            <h1>Problem Statement</h1>
            <p>
                Challenges in Personnel and Equipment Allocation: PetroEnergy
                Corp. operates in multiple geographically dispersed oil fields,
                making the allocation of personnel and equipment a significant
                logistical challenge. The company needs to find an efficient way
                to schedule and assign qualified workers and specific equipment
                to corresponding tasks at each site.
            </p>
        {/each}
    </main>
    <footer>
        <div class="sticky-panel">
            <hr class="subtle-divider mobile-styles" />
            <h1>About us</h1>
            <p>
                This case study focuses on the process of developing and
                implementing a resource management system for a leading company
                in the oil industry, named "PetroEnergy Corp."
            </p>
            <h1>Founded</h1>
            <p>Ontario City in 2020</p>
            <hr class="subtle-divider" />
            <h1>Next case study</h1>
            <p>
                <Link href="/">Tech Innovation in Retail</Link>
            </p>
        </div>
    </footer>
</div>

<style>
    /* Define styles for the page layout */
    .page-layout {
        padding: 0 40px;
        max-width: 1000px;
        margin: 80px auto;
        /* Set grid display with a gap */
        gap: 0 80px;
        display: grid;
    }

    /* Styles for paragraphs */
    p {
        color: #555;
        padding: 10px 0;
        line-height: 1.6;
    }

    /* Styles for the first paragraph in main if it doesn't contain an h1 element */
    main:not(:has(h1)) > p:first-child {
        padding: 20px 0;
    }

    /* Styles for heading level 1 */
    section h1 {
        color: #111;
        font-size: 2rem;
        font-weight: normal;
    }

    /* Styles for heading level 1 in main and footer */
    main h1,
    footer h1 {
        color: #111;
        padding-top: 20px;
        font-size: 1rem;
        font-weight: normal;
    }

    /* Styles for heading level 6 (Subtitle) */
    h6 {
        font-size: 1rem;
        font-weight: normal;
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
            grid-template-columns: 1fr 300px;
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
