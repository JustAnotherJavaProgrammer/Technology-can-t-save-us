<script lang="ts">
    import MetaInfo from "$lib/MetaInfo.svelte";
</script>

<MetaInfo title={undefined} />

<main>
    <span>Technology</span>
    <span>can't</span>
    <span>save</span>
    <span><span aria-hidden="true">.</span>us.</span>
</main>
<section>Not on its own.</section>

<style lang="scss">
    @import "src/styles.scss";

    main {
        @include main-column;
        min-height: 100lvh;

        font-size: clamp(1rem, 15vmin, 5rem);

        animation-name: colorshift;
        animation-duration: 12s;
        animation-iteration-count: infinite;
        animation-timing-function: steps(1);

        & > span {
            &:nth-child(1) {
                @include font-sans-serif;
            }
            &:nth-child(2) {
                @include font-serif;
            }
            &:nth-child(3) {
                @include font-cursive;
            }
            &:nth-child(4) {
                @include font-monospace;
                & > span:first-child {
                    visibility: hidden;
                }
            }
        }
    }

    @keyframes colorshift {
        @for $i from 1 through 13 {
            #{calc(100%/12)*(($i)-1)} {
                @include color-combo($i);
            }
        }
    }

    section {
        font-size: clamp(1rem, 15vmin, 5rem);
        text-align: center;
        padding: 1em;
    }
</style>
