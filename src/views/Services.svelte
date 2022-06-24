<script lang="ts">

    import ServiceCard from "../components/ServiceCard.svelte";

    interface ServiceType  {
        serviceName: string,
        serviceIcon: string,
        description: string,
        price: number,
    }
    
    function Service(
        name: string,
        icon: string,
        description: string,
        price: number
    ) {
        this.serviceName = name;
        this.serviceIcon = icon;
        this.description = description;
        this.price = price;
    }

    let serviceList: ServiceType[] = [
        new Service(
            "Hair cut",
            "fa-solid fa-scissors",
            "Regular men's or woman's hair cut",
            25
        ),
        new Service(
            "Shampooing",
            "fa-solid fa-soap",
            "Hair treatment for men or women",
            30
        ),
        new Service(
            "Special Cut",
            "fa-solid fa-scissors",
            "Extreme hair cuts, tribal hair, ect ...",
            40
        )
    ]

</script>

<section id="services">
    <h2 class="sectionTitle">Services</h2>
    <div class="cardContainer">
        {#each serviceList as service }
            <ServiceCard {...service}/>
        {/each}
    </div>
</section>

<style> 

    section { background-color: var(--primary); }

    @media screen and (min-width: 1000px) {

        .cardContainer {
            flex-flow: row wrap;
            justify-content: center;
        }

    }

</style>