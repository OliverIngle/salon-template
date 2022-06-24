<script lang="ts">
    export let 
        serviceName: string,
        serviceIcon: string,
        description: string,
        price: number;
</script>

<div class="container">
    <i class={serviceIcon}></i>
    <h3 class="name">{serviceName}</h3>
    <p>{description}</p>
    <div class="centerXContainer">
        <a class="priceTag" href="#booking">Book: {price} $</a>
    </div>
</div>

<style>

    .container {
        border: 3px solid var(--secondary);
        padding: 1rem;
        border-radius: 1rem;
        display: grid;
        grid-template-areas: 
            "icon name"
            "description description"
            "priceLink priceLink"
        ;
        grid-template-columns: 50% 50%;

        min-width: fit-content;
        overflow: hidden;
    }

    h3, i {
        font-size: 1.5rem;
        display: block;
    }

    h3 { grid-area: name; }

    i {
        text-align: center;
        grid-area: icon;
    }

    p {
        grid-area: description;
        text-align: center;
    }

    .priceTag {
        text-align: center;
        background-color: var(--tertiary);
        font-weight: bold;
        padding: 1rem 2rem 1rem 2rem;
        border-radius: 1rem;
        width: fit-content;
    }

    .centerXContainer {
        grid-area: priceLink;
    }

     @media screen and (min-width: 600px) and (max-width: 1000px) {

        .container {
            grid-template-areas:
                "icon name priceLink"
                "description description pricelink"
            ;
            grid-template-columns: 35% 35% 30%;

            padding-top: 4rem;
            padding-bottom: 4rem;
        }

        .centerXContainer {
            grid-row: span 2;
        }
    } 

    @media screen and (min-width: 1000px) {
        .container {
            width: 25rem;
            padding: 4rem;
        }
    }

</style>