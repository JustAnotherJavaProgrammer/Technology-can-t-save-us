<script lang="ts">
    import defaultImage from "$lib/assets/OpenGraph_Preview.png";

    import {page} from "$app/stores";
    export let title: string | undefined;
    export let description: string = "Technology can't save us. Not on its own.";
    export let image = defaultImage;
</script>

<svelte:head>
    <title>{title == undefined ? "" : title + " \u2013 "}Technology can't save us.</title>
    <meta name="description" content={description}>
    <!-- Open Graph Protocol: https://ogp.me/ -->
    <meta name="og:title" content={title ?? "Technology can't save us."}>
    <meta name="og:type" content="website">
    <meta name="og:image" content={image}>
    <meta name="og:url" content={$page.url.toString()}>
    <!-- Technically optional -->
    <meta name="og:description" content={description}>
    <meta name="og:locale" content="en_US">
    <meta name="og:site_name" content="Technology can't save us.">
</svelte:head>