<script lang="ts">

    const PHONE_NUMBER = "00 01 02 03 04";

    function copyNumber(e) {
        navigator.clipboard.writeText(PHONE_NUMBER);
        alert("Phone number copied to clipboard")
    }

</script>

<section id="booking">
    <h2 class="sectionTitle">Book your cut</h2>
    <div class="bookingInfoContainer">
        <div class="padded1margin1Block centerXContainer availability">
            <h3>Availability</h3>
            <i class="fa-regular fa-clock timeIcon"></i>
            <table>
                <tr>
                    <td>Mon -Sat</td>
                    <td>9AM - 5PM</td>
                </tr>
                <tr>
                    <td>Sunday</td>
                    <td class="red">Closed</td>
                </tr>
            </table>
        </div>
        <div class="centerXContainer padded1margin1Block phone">
            <h3>Phone</h3>
            <div class="phoneInfo">
                <div class="numberContainer">
                    <i class="fa-solid fa-phone"></i>
                    <address>{PHONE_NUMBER}</address>
                </div>
                <button on:click={copyNumber}>
                    <i class="fa-regular fa-clone copyIcon"></i>
                </button>
            </div>
        </div>
        <div class="padded1margin1Block contact">
            <h3>Contact</h3>
            <div class="contactForm">
                <form>
                    <label for="email">Email</label>
                    <input type="email" name="email" placeholder="Enter a valid email adress">
                    <label for="name">Name</label>
                    <input type="text" name="name" placeholder="Enter your name">
                    <label for="message">Message</label>
                    <textarea name="message" cols="30" rows="6" placeholder="Enter your message"></textarea>
                    <input type="submit" value="Submit" class="submitButton">
                </form>
            </div>
        </div>
    </div>
</section>

<style>

    section { background-color: var(--quarternary); }

    .padded1margin1Block {
        padding: 1rem;
        /* border: 3px solid var(--secondary);
        border-radius: 1rem; */
        margin: 1rem;
        margin-bottom: 0;
    }

    h3 {
        font-size: 1.5rem;
        align-self: flex-start;
    }

    i { font-size: 1.5rem; }
    i.timeIcon { padding-bottom: 1rem; }

    table {
        border-collapse: collapse;
        background-color: var(--primary);
    }
    tr:first-child td { padding: 1rem 1rem 0.5rem 1rem; }
    tr:last-child td { padding: 0.5rem 1rem 1rem 1rem; }
    tr:first-child { border-bottom: 2px solid var(--secondary); }
    .red { color: red; }
    address { font-size: 1.5rem; }

    .phoneInfo {
        margin-top: 1rem;
        display: flex;
    }

    .numberContainer {
        background-color: var(--primary);
        padding: 1rem;
        border-radius: 1rem;
        display: flex;
        gap: 1rem;
    }
    .numberContainer i {font-size: 1.5rem; }
    i.copyIcon { padding: 1rem; }

    .contactForm { margin-top: 1rem; }

    form {
        display: flex;
        flex-direction: column;
    }
    label {
        font-size: 1rem;
        font-weight: bold;
    }
    input, textarea {
        margin-bottom: 1rem;
        border-bottom: 2px solid var(--primary);
        padding: 1rem;
    }
    textarea {
        resize: none;
        height: 5rem;
    }

    input:focus, textarea:focus {
        border: 2px solid white;
        border-radius: 1rem;
        outline: none;
    }
    .submitButton {
        width: 100%;
        background-color: var(--primary);
        padding: 1rem;
        border-radius: 1rem;
    }

    @media screen and (min-width: 700px) {

        .padded1margin1Block:last-child {
            margin-bottom: 2rem;
        }

        .bookingInfoContainer {
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        h3 {
            align-self: auto;
            font-weight: bold;
        }

        i.timeIcon {
            visibility: hidden;
            height: 0px;
        }

        .contact {
            background-color: var(--primary);
            border-radius: 1rem;
            width: 30rem;
            padding: 2rem;
            padding-bottom: 1rem;
        }

        .availability, .phone {
            padding: 2rem;
            width: 30rem;
            border: 3px solid;
            border-color: var(--primary);
            border-radius: 1rem;
        }


        input, textarea {
            border-color: var(--tertiary);
        }

        .submitButton {
            background-color: var(--tertiary);
        }

    }



</style>