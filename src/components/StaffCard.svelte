<script lang="ts">

    export let 
        name: string,
        role: string,
        image: string;

</script>

<div class="card">
    <img src={image} alt={name}>
    <div class="info">
        <h3>{name}</h3>
        <p>{role}</p>
    </div>
</div>

<style>

    .card {
        border-bottom: 3px solid var(--secondary);
    }
    .card:last-child {
        border: none;
    }
    .card:last-child .info {
        padding-bottom: 0;
    }

    img {
        width: 100%;
        grid-area: image;
        border-radius: 2rem;
    }

    .info {
        padding: 1rem;
        display: flex;
        justify-content: space-evenly;
        align-items: center;
    }
    .info > * {
        margin: 0;
    }

    h3 {
        font-size: 1.5rem;
        font-weight: bold;
    }

</style>