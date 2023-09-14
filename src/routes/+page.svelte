<script lang="ts">
    import "$lib/css/global.css";
    import Link from "$lib/components/Link.svelte";
</script>

<svelte:head>
    <title>Ryan Kaylani</title>
</svelte:head>

<div class="layout">
    <!-- Static Section: Figure (Contains fixed content) -->
    <figure>
        <img
            width="92"
            height="92"
            src="https://avatars.githubusercontent.com/u/1137613?v=4"
            alt=""
        />
        <figcaption>
            <h1>Ryan Kaylani</h1>
            <p>Product Designer in Boston, MA, he/him</p>
        </figcaption>
    </figure>

    <!-- Dynamic Section: Main (Contains dynamic content) -->
    <main>
        <section>
            <h1>About</h1>
            <p>
                Ryan is a product manager from San Francisco. He's dedicated to
                creating innovative solutions that enhance our daily lives and
                empower us to excel in our endeavors. In his previous roles, he
                has contributed to the development of educational technology,
                entertainment applications, and financial services software.
                When he's not working, he enjoys exploring new hiking trails and
                camping in the great outdoors!
            </p>
        </section>
        <section>
            <h1>Work Experience</h1>
            <table>
                {#each Array(2) as _}
                    <tr>
                        <th>
                            <h1>2019 - 2019</h1>
                        </th>
                        <td>
                            <h1>
                                <Link href="/case/lorem-ipsum-dolor-sit">
                                    Development of a Resource Management System
                                    for the Oil Industry
                                </Link>
                            </h1>
                            <p>Ontario City, CA</p>
                            <p>
                                The company needs to find an efficient way to
                                schedule and assign qualified workers and
                                specific equipment to corresponding tasks at
                                each site.
                            </p>
                        </td>
                    </tr>
                {/each}
            </table>
        </section>
        <section>
            <h1>Contact</h1>
            <table>
                {#each Array(2) as _}
                    <tr>
                        <th>
                            <h1>Dribbble</h1>
                        </th>
                        <td>
                            <h1>
                                <Link href="/" external>zsfsw2</Link>
                            </h1>
                        </td>
                    </tr>
                    <tr>
                        <th>
                            <h1>Email</h1>
                        </th>
                        <td>
                            <h1>
                                <Link href="/" external>zsfsw2@gmail.com</Link>
                            </h1>
                        </td>
                    </tr>
                    <tr>
                        <th>
                            <h1>Twitter</h1>
                        </th>
                        <td>
                            <h1>
                                <Link href="/" external>zsfsw2</Link>
                            </h1>
                        </td>
                    </tr>
                {/each}
            </table>
        </section>
    </main>
</div>

<style>
    /* Styles for the page layout */
    .layout {
        gap: 0 80px;
        display: grid;
        /* Layout Behavior */
        padding: 0 40px;
        max-width: 620px;
        margin: 80px auto;
    }

    /* Styles for the figure section */
    figure {
        gap: 20px;
        display: flex;
        align-items: center;
        /* Figure Behavior */
        margin-bottom: 40px;
    }

    /* Styles for the figure image */
    figure img {
        width: 92px;
        height: 92px;
        border-radius: 92px;
    }

    /* Styles for the figure caption heading */
    figure figcaption h1 {
        color: #111;
        line-height: 1.6;
        font-size: 1.4rem;
        font-weight: normal;
    }

    /* Styles for the figure caption paragraph */
    figure figcaption p {
        color: #777;
        line-height: 1.6;
        font-size: 1rem;
        font-weight: normal;
    }

    /* Styles for the main section */
    main section table {
        gap: 20px;
        display: grid;
    }

    /* Styles for table rows in the main section */
    main section table tr {
        gap: 20px;
        display: flex;
    }

    /* Styles for table headers in the main section */
    main section table th {
        min-width: 80px;
        text-align: left;
    }

    /* Styles for section headings in the main section */
    main section h1 {
        color: #111;
        line-height: 1.6;
        font-size: 1rem;
        font-weight: normal;
        /* Section Header Behavior */
        margin-top: 20px;
        margin-bottom: 10px;
    }

    /* Styles for section paragraphs in the main section */
    main section p {
        color: #777;
        line-height: 1.6;
        font-size: 1rem;
        font-weight: normal;
    }

    /* Styles for section paragraphs in the main section, except the last one */
    main section p:not(:last-child) {
        /* Section Paragraph Behavior */
        margin-bottom: 2px;
    }

    /* Styles for table header within the main section */
    main section table th h1 {
        color: #777;
    }

    /* Styles for table headers in the main section */
    main section table h1 {
        /* Table Header Behavior */
        margin-top: 0px;
    }

    /* Add scroll padding to body and html elements */
    :global(body, html) {
        scroll-padding-top: 40px;
    }
</style>
