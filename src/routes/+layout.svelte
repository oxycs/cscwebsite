<script lang="ts">
import Navbar from "$lib/components/navbar.svelte";
import Footer from "$lib/components/footer.svelte";
import FloatingBox from "$lib/components/floatingBox.svelte";
</script>

<link rel="stylesheet" href="/global.css" />


<div class="navbar"><Navbar /></div>
<div class="content"><slot /></div>
<div class="footer"><Footer /></div>

<style>
    /* add padding to top of content of 5vh */
    :global(body) {
        padding-top: 7vh;
        margin-left: 0px;
        margin-right: 0px;
        /* background-image: url('/img/2018-0608_JacarandaTrees-07.jpg');
        background-size: cover;
        background-repeat: no-repeat;
        background-attachment: fixed;
        background-position: center; */
    }

    .content {
        position: relative;
        min-height: 100vh;
    }

    .footer {
        /* position: absolute;
        bottom: 0;
        left:0; */
        width: 100%;
    }
</style>