<header class="fullscreenCenter">
    <div class="centerXContainer landingContent">
        <h1>Salon Template</h1>
        <div class="centerXContainer">
            <a href="#booking" class="downLink">Book</a>
        </div>
    </div>
</header>

<style>
    
    header {
        background-image: url("../images/landing-image-0.jpg");
        background-size: cover;
        color: white;
    }

    .fullscreenCenter {
        height: 100vh;
        display: flex;
        /* justify-content: center; */
        align-items: center;
    }

    .landingContent {
        width: 100%;
        background-color: rgba(0, 0, 0, 0.5);
        padding: 2rem;
        /* border-radius: 1rem; */
    }

    h1 {
        font-size: 2rem;
        font-weight: bold;
        margin-bottom: 1rem;
        color: var(--primary);
    }

    .downLink {
        background-color: var(--tertiary);
        font-weight: bold;
        flex-grow: 0;
        padding: 1rem 2rem 1rem 2rem;
        border-radius: 1rem;
        width: fit-content;
    }

    .downLink:focus {
        border: 2px solid var(--secondary);
    }

    @media screen and (min-width: 800px) {

        header {
            background-image: url("../images/landing-image-800.jpg");
        }

        .fullscreenCenter {
            justify-content: center;
        }

        .landingContent {
            width: auto;
            border-radius: 1rem;
        }

    }

    @media screen and (min-width: 1200px) {

        .fullscreenCenter {
            align-items: flex-end;
        }

        .landingContent {
            width: 100%;
            border-radius: 0;
        }


    }    

</style>