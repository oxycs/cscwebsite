<script lang="ts">
    import Arrowitem from "$lib/components/arrowitem.svelte";
    import { discordURL, emailAddr } from "../../constants";
</script>

<div class="page">

    <Arrowitem img="/img/discordbg169.png" imgalt="Discord Logo" title="Join the CSC Discord!" description="Join our Discord to chat with other CS students and get help with your work!" url={discordURL}></Arrowitem>
    <Arrowitem img="/img/gmailscreenshot.png" imgalt="Gmail Screenshot" title="Loooking for advice/mentorship from an upperclassmen?" description="Join our buddy system! We can pair you with a student eager to help out." url={emailAddr}></Arrowitem>
    <Arrowitem img="/img/SCR-20250126-rme.png" imgalt="Q&A PDF" title="Have a burning question about Computer Science at Oxy?" description="We've answered as many as we could in this Computer Science Q&A" url="/pdf/qa.pdf"></Arrowitem>
    <Arrowitem img="/img/SCR-20250126-rnl.png" imgalt="Opportunities Mailing List Screenshot" title="Stay up to date on internship and research opportunities" description="Join the CS Department's opportunities mailing list!" url="https://groups.google.com/a/oxy.edu/g/compsci-opportunities-g"></Arrowitem>
    <Arrowitem img="/img/serverroom.jpg" imgalt="Server Room" title="Need a place to host your CS project?" description="We'll host it for you on the Computer Science Club's server! Email us to learn more." url={emailAddr}></Arrowitem>

    
    <p class="heading">Past Presentations and Workshops</p>
    <p class="heading">Academic Support</p>
    <p class="content">Workspace is a place where students come together to work on CS projects and coursework. It is a great opportunity to make connections with other CS students and get help from them. Additionally, tutors who work for Oxy's Scientific Scholars Achievement Program (SSAP), a student-led academic support organization, as well as class TAs are available for further help.</p>
    <p class="content">Workspace & SSAP Hours</p>
    <p class="content">Sun, 6-8 pm PST</p>
    <p class="content">Tues, 6-8 pm PST</p>
    <p class="heading">Career Support</p>
</div>

<style>

    .content {
        font-size: 1.5vh;
        margin:0;
    }

    .heading {
        font-size: 2vh;
        margin-bottom:0.8vh;
    }

    .page {
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
        font-family: "Nunito", sans-serif;
        margin:0px;
    }

    .orangetext {
        color: rgb(253, 115, 70);
        text-decoration: none;
    }

    p {
    }

</style>