<script lang="ts">

</script>

<div class="page">
    <p>Our mission is to create an inclusive and collaborative community around Computer Science and provide resources and opportunities for all Oxy students</p>

    <div class="membercontainer">

        <div class="member">
            <img src="/img/placeholder.png" alt="Portrait photograph member">
            <p class="name">Alyanna McGrath</p>
            <p class="title">President</p>
        </div>
        <div class="member">
            <img src="/img/placeholder.png" alt="Portrait photograph member">
            <p class="name">Nick Novak</p>
            <p class="title">President</p>
        </div>
        <div class="member">
            <img src="/img/placeholder.png" alt="Portrait photograph member">
            <p class="name">Ethan Schoen</p>
            <p class="title">Head of Finance</p>
        </div>
        <div class="member">
            <img src="/img/placeholder.png" alt="Portrait photograph member">
            <p class="name">Liv Gilbert-Adler</p>
            <p class="title">Head of Projects</p>
        </div>
        <div class="member">
            <img src="/img/placeholder.png" alt="Portrait photograph member">
            <p class="name">Tiffany Mo</p>
            <p class="title">Head of Marketing</p>
        </div>
        <div class="member">
            <img src="/img/placeholder.png" alt="Portrait photograph member">
            <p class="name">Brian Cuellar</p>
            <p class="title">Head of Community Engagement</p>
        </div>
        <div class="member">
            <img src="/img/placeholder.png" alt="Portrait photograph member">
            <p class="name">Roselyn Chin</p>
            <p class="title">Head of Community Engagement</p>
        </div>
        <div class="member">
            <img src="/img/placeholder.png" alt="Portrait photograph member">
            <p class="name">Jadriel Delim</p>
            <p class="title">Head of Event Coordination</p>
        </div>

    </div>
</div>

<style>
    .page {
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
        font-family: "Nunito", sans-serif;
    }

    .page > p {
        font-size: 2vh;
        text-align: center;
    }

    .membercontainer {
        display: flex;
        justify-content: center;
        align-items: start;
        flex-flow: row wrap;
        margin-top: 1vh;
        width:100%;
        text-align:center;
    }

    .member {
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
        margin-left: 1vw;
        margin-right: 1vw;
        max-width: 20vh;
    }

    .member > img {
        width: 20vh;
        height: 20vh;
        border-radius: 50%;
    }

    .name {
        font-size: 2.5vh;
        font-weight: bold;
        margin: 0;
    }

    .title {
        font-size: 2vh;
        margin: 0;
        width: 100%;
    }
</style>