<script lang="ts">
    import "@fontsource/oswald";
    import "@fontsource/lora";
    import "@fontsource/caveat-brush";
    import "@fontsource/courier-prime";
    import Footer from "$lib/Footer.svelte";
</script>

<slot />
<Footer />

<style lang="scss">
    @import "src/styles.scss";

    :global(html) {
        scroll-behavior: smooth;
        height: 100%;
        // margin: 0;
        // padding: 0;
        // min-width: 100%;
        @include color-combo-1;
        @media (prefers-color-scheme: dark) {
            @include color-combo-2;
        }
    }

    :global(body) {
        // padding: 0;
        // margin: 0;
        scroll-behavior: smooth;
        height: 100%;
        // min-width: 100%;
        display: flex;
        flex-direction: column;
        align-items: stretch;
        justify-content: stretch;
        gap: 0;
        @include font-sans-serif;
    }

    :global(*) {
        box-sizing: border-box;
        padding: 0;
        margin: 0;
    }

    :global(a) {
        color: inherit;
        text-decoration: underline;
    }
</style>
