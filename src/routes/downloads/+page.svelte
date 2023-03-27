<script lang="ts">
    import { preloadData } from "$app/navigation";

    import zero from "$lib/assets/Technology can_t save us/Technology can_t save us_0.png";
    //@ts-expect-error
    import zero_small from "$lib/assets/Technology can_t save us/Technology can_t save us_0.png?width=200";
    import one from "$lib/assets/Technology can_t save us/Technology can_t save us_1.png";
    //@ts-expect-error
    import one_small from "$lib/assets/Technology can_t save us/Technology can_t save us_1.png?width=200";
    import two from "$lib/assets/Technology can_t save us/Technology can_t save us_2.png";
    //@ts-expect-error
    import two_small from "$lib/assets/Technology can_t save us/Technology can_t save us_2.png?width=200";
    import three from "$lib/assets/Technology can_t save us/Technology can_t save us_3.png";
    //@ts-expect-error
    import three_small from "$lib/assets/Technology can_t save us/Technology can_t save us_3.png?width=200";
    import four from "$lib/assets/Technology can_t save us/Technology can_t save us_4.png";
    //@ts-expect-error
    import four_small from "$lib/assets/Technology can_t save us/Technology can_t save us_4.png?width=200";
    import five from "$lib/assets/Technology can_t save us/Technology can_t save us_5.png";
    //@ts-expect-error
    import five_small from "$lib/assets/Technology can_t save us/Technology can_t save us_5.png?width=200";
    import six from "$lib/assets/Technology can_t save us/Technology can_t save us_6.png";
    //@ts-expect-error
    import six_small from "$lib/assets/Technology can_t save us/Technology can_t save us_6.png?width=200";
    import seven from "$lib/assets/Technology can_t save us/Technology can_t save us_7.png";
    //@ts-expect-error
    import seven_small from "$lib/assets/Technology can_t save us/Technology can_t save us_7.png?width=200";
    import eight from "$lib/assets/Technology can_t save us/Technology can_t save us_8.png";
    //@ts-expect-error
    import eight_small from "$lib/assets/Technology can_t save us/Technology can_t save us_8.png?width=200";
    import nine from "$lib/assets/Technology can_t save us/Technology can_t save us_9.png";
    //@ts-expect-error
    import nine_small from "$lib/assets/Technology can_t save us/Technology can_t save us_9.png?width=200";
    import ten from "$lib/assets/Technology can_t save us/Technology can_t save us_10.png";
    //@ts-expect-error
    import ten_small from "$lib/assets/Technology can_t save us/Technology can_t save us_10.png?width=200";
    import eleven from "$lib/assets/Technology can_t save us/Technology can_t save us_11.png";
    //@ts-expect-error
    import eleven_small from "$lib/assets/Technology can_t save us/Technology can_t save us_11.png?width=200";
    import MetaInfo from "$lib/MetaInfo.svelte";

    const images: { img: string; small: string }[] = [
        { img: zero, small: zero_small },
        { img: one, small: one_small },
        { img: two, small: two_small },
        { img: three, small: three_small },
        { img: four, small: four_small },
        { img: five, small: five_small },
        { img: six, small: six_small },
        { img: seven, small: seven_small },
        { img: eight, small: eight_small },
        { img: nine, small: nine_small },
        { img: ten, small: ten_small },
        { img: eleven, small: eleven_small },
    ];
</script>

<MetaInfo title="Downloads" description="Download the design from the homepage in a vertical 3:2 format." />

<main>
    <h1>Downloads</h1>
    <p>
        On this page, you can download the design from the homepage in a vertical 3:2 format. You are free to them as you want.<br />
        The images below are licensed under
        <a href="https://creativecommons.org/publicdomain/zero/1.0/" target="_blank">CC0 1.0 Universal (CC0 1.0) &ndash; Public Domain Dedication</a>.<br />
        Click on an image to open it in a new tab. You can then right-click on (or long-tap on a touchscreen) the image and select "Save image as..." to download it.
    </p>
    <section>
        {#each images as image, i}
            <a href={image.img} target="_blank">
                <img width="200" height="300" src={image.small} alt={`Technology can't save us, variant ${i + 1}`} />
            </a>
        {/each}
    </section>
</main>

<style lang="scss">
    @import "src/styles.scss";

    main {
        @include main-column;
        justify-content: center;
        padding: 1rem;
    }

    p {
        margin-bottom: 1rem;
    }

    section {
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
        flex-direction: row;
        gap: 1rem;
        @media screen and (min-width: ((200px*3) + (2*16px))) {
            display: grid;
            grid-template-columns: 1fr 1fr 1fr;
            grid-auto-rows: 1fr;
        }
    }

    img {
        object-fit: cover;
        border: 1px solid $black;
        @media (prefers-color-scheme: dark) {
            border-color: $white;
        }
    }
</style>
