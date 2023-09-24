<script>
    import { page } from "$app/stores";
</script>

<main>
<h1>{$page.status} &ndash; {$page.error?.message ?? "That's an error"}</h1>
<p>
    This is not the page you are looking for.<br />
    <a href="/">Go back to the home page</a>
</p>
</main>

<style lang="scss">
    @import "src/styles.scss";

    main {
        @include main-column;
        justify-content: center;
    }
</style>