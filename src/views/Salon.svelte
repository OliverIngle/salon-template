<script lang="ts">
    
    import GridImage from "../components/GridImage.svelte";

    type dimention = "tall" | "wide" | "tall wide" | null;
    interface ImageInfo {
        url: string,
        dimentions: dimention,
    }

    function Image(name: string, dimentions: dimention) {
        this.url = `../images/${name}.jpg`;
        this.dimentions = dimentions;
    }

    let imageList: ImageInfo[] = [
        new Image("salon1", null),
        new Image("salon2", "tall"),
        new Image("salon3", null),
        new Image("salon9", "tall"),
        new Image("salon4", null),
        new Image("salon5", null),
        new Image("salon6", "tall wide"),
        new Image("salon7", null),
        new Image("salon8", null),
    ];
    
</script>

<section id="salon">
    <h2 class="sectionTitle">The salon</h2>
    <div class="imageGrid">
        {#each imageList as image }
            <GridImage {...image} />
        {/each}
    </div>
</section>

<style>

    section {
        background-color: var(--quarternary);
    }

    .imageGrid {
        padding: 1rem;
        display: grid;
        gap: 1rem;

        grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
        grid-auto-rows: 240px;
    }

</style>