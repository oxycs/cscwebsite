<script lang="ts">
</script>

<div class="main">
    <div class="title">
        <span class="blacktext"><p>Computer</p></span>
        <span class="orangetext"><p>Science</p></span>
        <span class="blacktext"><p>Club</p></span>
    </div>
    <a href="/what-we-do"><button>What We Do</button></a>
    <p>Our mission is to create an inclusive and collaborative community around Computer Science and provide resources and opportunities for all Oxy students.</p>
</div>

<style>
    .main {
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
        font-family: "Nunito", sans-serif;
    }

    .title {
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
        font-size: 10vh;
    }

    .blacktext {
        color: rgb(45,46,46);
    }

    .orangetext {
        color: rgb(253, 115, 70);
    }

    .title > span > p {
        margin: 0;
        font-size:10vh;
    }

    button {
        background-color: rgb(253, 115, 70);
        color: white;
        border: none;
        border-radius: 5px;
        padding: 1vh;
        font-size: 2vh;
        font-family: "Nunito", sans-serif;
        margin-top: 3vh;
        margin-bottom:3vh;
    }

    .main > p {
        font-size: 2vh;
        text-align: center;
        padding-left: 5vw;
        padding-right: 5vw;
    }
</style>