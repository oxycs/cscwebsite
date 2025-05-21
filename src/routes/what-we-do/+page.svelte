<script lang="ts">
    import Fa from 'svelte-fa'
    import { faGithub, faDiscord, faInstagram, faLinkedin } from '@fortawesome/free-brands-svg-icons' 
    import { faOtter } from '@fortawesome/free-solid-svg-icons'
    import { raftrURL, githubURL, discordURL, instaURL, linkedInURL, emailAddr, emailPlaintext } from '../../constants';
</script>

<div class="page">
    <span class="title"><p>What we do at the Oxy Computer Science Club</p></span>

    <div class="lines">
        <p>🧑‍🤝‍🧑 Throw a social events, so that members can meet</p>
        <p>📅 Host events to discuss topics in technology</p>
        <p>📽️ Oversee the completion of collaborative open-source projects</p>
        <p>🌱 Hold workspaces, as a hub for collaboration</p>
        <p>🗳️ Voice student input in CS department meetings</p>
        <p>🤝 Manage a buddy system to connect students with mentors</p>
        <p>📧 Maintain a mailing list for internships, employment, and other CS topics</p>
        <p>🖥️ Host projects on a server</p>
    </div>

    <span class="endline"><p> Got any more questions? Email us at <span class="orangetext"><a href={emailAddr}>{emailPlaintext}</a></span>, or check out our Q&A on commonly asked questions at the <span class="orangetext"><a href="/resources">resources</a></span> page!</p></span>

    <div class="socials">
        <p>Find us here!</p>
        <ul>
            <li><div class="faIcon"><a href={raftrURL} target="_blank"><Fa icon={faOtter} /></a></div></li>
            <li><div class="faIcon"><a href={githubURL} target="_blank"><Fa icon={faGithub} /></a></div></li>
            <li><div class="faIcon"><a href={discordURL} target="_blank"><Fa icon={faDiscord} /></a></div></li>
            <li><div class="faIcon"><a href={instaURL} target="_blank"><Fa icon={faInstagram} /></a></div></li>
            <li><div class="faIcon"><a href={linkedInURL} target="_blank"><Fa icon={faLinkedin} /></a></div></li>
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