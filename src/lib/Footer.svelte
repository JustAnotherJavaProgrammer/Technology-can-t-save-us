<footer>
    <nav>
        <a href="/">Home</a>
        <a href="/downloads">Downloads</a>
        <a href="/legal/imprint">Imprint</a>
        <a href="/legal/privacypolicy">Privacy Policy</a>
        <a href="/legal/impressum">Impressum</a>
        <a href="/legal/datenschutzerklaerung">Datenschutzerklärung</a>
    </nav>
</footer>

<style lang="scss">
    @import "src/styles.scss";

    footer {
        padding: 0.5rem;
        @include color-combo-2;
        @media (prefers-color-scheme: dark) {
            @include color-combo-1;
        }
    }

    footer, nav {
        display: flex;
        flex-direction: row;
        justify-content: center;
        align-items: center;
        gap: 0.5rem;
    }
</style>