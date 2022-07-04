<script lang="ts">
    import StaffCard from "../components/StaffCard.svelte";

    interface StaffType {
        name: string,
        role: string,
        image: string,
    }

    function TeamMember(
        name: string,
        role: string,
        image: string
    ) {
        this.name = name;
        this.role = role;
        this.image = image;
    }

    let teamMembers: StaffType[] =[
        new TeamMember(
            "Cindy",
            "Lead hair dresser",
            "../images/cindy.jpg"
        ),
        new TeamMember(
            "Alice",
            "Hair dresser",
            "../images/alice.jpg"
        ),
        new TeamMember(
            "Jacob",
            "Barber",
            "../images/jacob.jpg"
        ),
    ] 
</script>

<section id="team">
    <h2 class="sectionTitle">The team</h2>
    <div class="cardContainer">
        {#each teamMembers as member }
            <StaffCard {...member} />
        {/each}
    </div>
</section>

<style>

    section {
        background-color: var(--primary);
    }

    @media screen and (min-width: 650px) {

        .cardContainer {
            display: flex;
            flex-direction: row;
            flex-wrap: wrap;

            justify-content: center;
        }

    }

</style>