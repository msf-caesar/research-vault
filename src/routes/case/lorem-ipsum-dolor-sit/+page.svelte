<script lang="ts">
    import "$lib/css/global.css";
    import Link from "$lib/components/Link.svelte";
    import ShareLink from "$lib/components/ShareLink.svelte";
</script>

<svelte:head>
    <title>
        Case Study - Development of a Resource Management System for the Oil
        Industry
    </title>
</svelte:head>

<div class="layout">
    <!-- Static Section: Header (Contains fixed content) -->
    <section>
        <p>Case Study</p>
        <h1>
            Development of a Resource Management System for the Oil Industry
        </h1>
        <hr class="divider" />
    </section>

    <!-- Static Section: Main Content (Contains repetitive content) -->
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

    <!-- Static Section: Footer (Contains fixed content) -->
    <footer>
        <div class="footer-sticky">
            <hr class="divider divider--subtle divider--mobile" />

            <h1>About</h1>
            <p>
                This section focuses on the development of PetroEnergy Corp.'s
                resource management system in the oil industry.
            </p>

            <h1>Founded</h1>
            <p>Ontario City in 2020</p>

            <hr class="divider divider--subtle" />

            <h1>Next case study</h1>
            <p><Link href="/">Tech Innovation in Retail</Link></p>

            <hr class="divider divider--subtle" />
            <p><Link href="/">Back to profile</Link></p>
            <p>
                <ShareLink
                    data={{
                        title: "MDN",
                        text: "Learn web development on MDN!",
                        url: "https://developer.mozilla.org",
                    }}
                >
                    Share
                </ShareLink>
            </p>
        </div>
    </footer>
</div>

<style>
    /* Define styles for the page layout */
    .layout {
        gap: 0 80px;
        display: grid;
        /* Behavior */
        padding: 0 40px;
        max-width: 1000px;
        margin: 80px auto;
    }

    /* Styles for headings and text */
    main h1,
    footer h1 {
        color: #111;
        line-height: 1.6;
        font-size: 1rem;
        font-weight: normal;
        /* Behavior */
        margin-top: 20px;
        margin-bottom: 10px;
    }

    /* Styles for main text in the content */
    main p,
    footer p {
        color: #666;
        line-height: 1.6;
        font-size: 1rem;
        font-weight: normal;
    }

    /* Define spacing between text paragraphs */
    main p:not(:last-child),
    footer p:not(:last-child) {
        /* Behavior */
        margin-bottom: 10px;
    }

    /* Styles for the category label in the section */
    section p {
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
    section h1 {
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
        .layout {
            grid-template-columns: 1fr 300px; /* Two-column layout */
        }

        /* Sticky footer for larger screens */
        .footer-sticky {
            top: 40px;
            position: sticky;
        }

        /* Grid positioning for section on larger screens */
        section {
            grid-column: 1 / 2;
            grid-row: 1 / 2;
        }

        /* Grid positioning for main content on larger screens */
        main {
            grid-column: 1 / 2;
            grid-row: 2 / 3;
        }

        /* Grid positioning for footer on larger screens */
        footer {
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
