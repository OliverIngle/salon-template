<script lang="ts">
    export let
        url: string,
        dimentions: any;

    let style = `background-image: url(${url})`;

</script>

<div class={dimentions} style={style}></div>

<style>
    
    div {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        background: #353535;
        font-size: 3rem;
        color: #fff;
        /* box-shadow: rgba(3, 8, 20, 0.1) 0px 0.15rem 0.5rem, rgba(2, 8, 20, 0.1) 0px 0.075rem 0.175rem; */
        height: 100%;
        width: 100%;
        border-radius: 4px;
        transition: all 500ms;
        overflow: hidden;

        background-size: cover;
        background-position: center;
        background-repeat: no-repeat;
    }

    @media screen and (min-width: 600px) {
        .tall { grid-row: span 2 / auto; }
        .wide { grid-column: span 2 / auto; }
    }
    

</style>