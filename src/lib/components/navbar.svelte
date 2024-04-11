<script lang="ts">
    import Borger from "./borger.svelte";
</script>



<nav>
<img class="logoimg" src="/img/oxyos-logo.svg" alt="Computer Science Club Logo">
<div class="hamburger">
    <Borger />
</nav>

<style>
    nav {
        background-color: white;
        color: #555;
        width: 100%;
        position:absolute;
        left:0px;
        top:0px;
        min-height:7vh;
    }

    .logoimg {
        height: 6vh;
        padding-left: 10vw;
        padding-top: 0.5vh;
        position: absolute;
    }

    .hamburger {
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
        min-height: 7vh;
    }
</style>