<script lang="ts">
    export let href: string;
    export let external: boolean = false;

    let props: Record<string, string | boolean> = {};

    if (external) {
        props = {
            target: "_blank",
            rel: "noopener noreferrer",
        };
    }
</script>

<a {href} {...props}>
    <slot />
</a>
