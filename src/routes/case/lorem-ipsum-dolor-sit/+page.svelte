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

<div class="page">
    <!-- Static section for section study information -->
    <section class="section">
        <!-- Category Information -->
        <p class="section__category">Case Study</p>

        <!-- Main Heading -->
        <h1 class="section__title">
            Development of a Resource Management System for the Oil Industry
        </h1>

        <!-- Horizontal Rule Divider -->
        <hr class="divider" />
    </section>

    <!-- Dynamic main area -->
    <main class="main">
        <!-- Loop through an array of challenges -->
        {#each Array(10) as _}
            <!-- Dynamic heading and paragraph for challenges -->
            <h1 class="main__title">
                Challenges in Personnel and Equipment Allocation
            </h1>
            <p class="main__text">
                Challenges in Personnel and Equipment Allocation: PetroEnergy
                Corp. operates in multiple geographically dispersed oil fields,
                making the allocation of personnel and equipment a significant
                logistical challenge. The company needs to find an efficient way
                to schedule and assign qualified workers and specific equipment
                to corresponding tasks at each site.
            </p>
        {/each}
    </main>

    <!-- Dynamic footer with company information -->
    <footer class="footer">
        <div class="footer__sticky">
            <!-- Horizontal Rule Divider -->
            <hr class="divider divider--subtle divider--mobile" />

            <!-- About PetroEnergy Corp. -->
            <h1 class="footer__title">About</h1>
            <p class="footer__text">
                This section study focuses on PetroEnergy Corp.'s resource
                management system development in the oil industry.
            </p>

            <!-- Company founding information -->
            <h1 class="footer__title">Founded</h1>
            <p class="footer__text">Ontario City in 2020</p>

            <!-- Horizontal Rule Divider -->
            <hr class="divider divider--subtle" />

            <!-- Next section study link -->
            <h1 class="footer__title">Next</h1>
            <p class="footer__text">
                <Link href="/">Tech Innovation in Retail</Link>
            </p>
        </div>
    </footer>
</div>

<style>
    /* Define styles for the page layout */
    .page {
        gap: 0 80px;
        display: grid;
        /* Behavior */
        padding: 0 40px;
        max-width: 1000px;
        margin: 80px auto;
    }

    /* Styles for headings and text */
    .main__title,
    .footer__title {
        color: #111;
        line-height: 1.6;
        font-size: 1rem;
        font-weight: normal;
        /* Behavior */
        margin-top: 20px;
        margin-bottom: 10px;
    }

    /* Styles for main text in the content */
    .main__text,
    .footer__text {
        color: #555;
        line-height: 1.6;
        font-size: 1rem;
        font-weight: normal;
    }

    /* Define spacing between text paragraphs */
    .main__text:not(:last-child),
    .footer__text:not(:last-child) {
        /* Behavior */
        margin-bottom: 10px;
    }

    /* Styles for the category label in the section */
    .section__category {
        line-height: 1.6;
        font-size: 1rem;
        font-weight: normal;
        /* Gradient text color */
        color: transparent;
        background-clip: text;
        background-image: linear-gradient(to bottom left, #0b68cb, #113264);
        /* Behavior */
        margin-bottom: 10px;
    }

    /* Styles for heading level 1 in the section */
    .section__title {
        color: #111;
        font-size: 2rem;
        font-weight: normal;
    }

    /* Styles for horizontal rule (divider) */
    .divider {
        border: none;
        border-top: solid 1px #dddde4;
        /* Behavior */
        margin-top: 40px;
    }

    /* Styles for a subtle divider */
    .divider--subtle {
        width: 40px;
        /* Behavior */
        margin-bottom: 40px;
    }

    /* Media query for larger screens */
    @media only screen and (min-width: 880px) {
        /* Reset mobile-specific styles for the divider */
        .divider--mobile {
            all: unset;
        }
        /* Adjust page layout for larger screens */
        .page {
            grid-template-columns: 1fr 300px; /* Two-column layout */
        }
        /* Sticky footer for larger screens */
        .footer__sticky {
            top: 40px;
            position: sticky;
        }
        /* Grid positioning for section on larger screens */
        .section {
            grid-column: 1 / 2;
            grid-row: 1 / 2;
        }
        /* Grid positioning for main content on larger screens */
        .main {
            grid-column: 1 / 2;
            grid-row: 2 / 3;
        }
        /* Grid positioning for footer on larger screens */
        .footer {
            grid-column: 2 / 3;
            grid-row: 2 / 3;
            /* Behavior */
            position: relative;
        }
    }

    /* Add scroll padding to body and html elements */
    :global(body, html) {
        scroll-padding-top: 40px;
    }
</style>
