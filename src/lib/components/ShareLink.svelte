<script lang="ts">
    export let data: Record<string, string>;
</script>

<button
    on:click={(e) => {
        try {
            navigator.share(data);
        } catch (err) {
            if (e.target instanceof HTMLElement) {
                e.target.textContent = "Your browser can't share";
            }
        }
    }}
>
    <slot />
</button>

<style>
    button {
        all: unset;
        color: #111;
        text-decoration: underline;
        text-decoration-color: #dddde4;
        /* Behavior a link */
        cursor: pointer;
    }
</style>
