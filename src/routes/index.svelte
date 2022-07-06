<script lang="ts">
    import AboutComponent from "../lib/components/AboutComponent.svelte";
    import LinksComponent from "../lib/components/LinksComponent.svelte";
</script>

<main>
    <AboutComponent/>
    <LinksComponent/>
</main>


<style>
    @media (min-width: 640px) {
        main {
            max-width: none;
        }
    }

    main {
        margin: 0;
    }
</style>