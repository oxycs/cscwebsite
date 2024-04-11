<script lang="ts">
    import Fa from 'svelte-fa'
    import { faSlack, faGithub, faFacebook, faInstagram } from '@fortawesome/free-brands-svg-icons' 
</script>

<div class="page">
    <span class="title"><p>What we do at Oxy Open Source</p></span>

    <div class="lines">
        <p>🧑‍🤝‍🧑 Throw a social hour every friday</p>
        <p>📅 Host an event every two weeks</p>
        <p>📽️ Oversee the completion of four open-source projects, annually</p>
        <p>🌱 Hold Workspace, a hub for collaboration, two times a week</p>
        <p>🗳️ Voice student input in CS department meetings</p>
        <p>🤝 Manage a buddy system to connect students with mentors</p>
    </div>

    <span class="endline"><p> Got any more questions? Email us at <span class="orangetext"><a href="mailto:opensource@oxy.edu">opensource@oxy.edu</a></span>, or check out our Q&A on commonly asked questions at the <span class="orangetext"><a href="/resources">resources</a></span> page!</p></span>

    <div class="socials">
        <p>Find us here!</p>
        <ul>
            <li><div class="faIcon"><a href="https://example.com"><Fa icon={faSlack} /></a></div></li>
            <li><div class="faIcon"><a href="https://example.com"><Fa icon={faGithub} /></a></div></li>
            <li><div class="faIcon"><a href="https://example.com"><Fa icon={faFacebook} /></a></div></li>
            <li><div class="faIcon"><a href="https://example.com"><Fa icon={faInstagram} /></a></div></li>
        </ul>
    </div>
</div>


<style>
    .page {
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
        font-family: "Nunito", sans-serif;
        margin:0px;
    }

    .title {
        font-size: 4vh;
        margin:0px;
        font-weight: 400;
    }

    .lines {
        font-size: 2vh;
        margin:0px;
    }

    .endline {
        font-size: 1.5vh;
        margin:0px;
    }

    .orangetext > a {
        color: rgb(253, 115, 70);
        text-decoration: none;
    }

    .socials {
        font-size: 2vh;
        font-weight: bold;
        margin:0px;
        text-align: center;
        padding: 0px;
    }

    .socials > ul {
        display: flex;
        list-style-type: none;
        justify-content: center;
        padding: 0;
        margin: 0;
    }

    .socials > ul > li {
        padding-left: 0.15vw;
        padding-right: 0.15vw;
        font-size: 3.5vh;
    }

    .faIcon > a {
        color: #555;
        text-decoration: none;
    }

    .socials > p {
        margin:0px;
    }
</style>