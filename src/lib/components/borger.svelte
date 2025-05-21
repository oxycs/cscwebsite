<script lang="ts">
import Fa from 'svelte-fa'
import { faBars, faS } from '@fortawesome/free-solid-svg-icons'
import { faGithub, faDiscord, faInstagram, faLinkedin } from '@fortawesome/free-brands-svg-icons'
import { faOtter } from '@fortawesome/free-solid-svg-icons'
import { onMount } from 'svelte'
import { page } from '$app/stores'; 
import { raftrURL, githubURL, discordURL, instaURL, linkedInURL } from '../../constants'

let expanded = false
let loaded = false

// wait for onMount to finish before running toggle. onMount waits for the document to hydrate.
onMount(() => {
    loaded = true
    page.subscribe(value => {
        document.querySelector("."+value.url.pathname.toString().replace("/", "")).classList.add('active')
        document.querySelector("."+value.previous.url.pathname.toString().replace("/", "")).classList.remove('active')
    })
})

function toggle() {
    if (loaded) {
        expanded = !expanded
        if (expanded) {
            document.querySelector('.expanded').classList.remove('nodisplay')
        } else {
            document.querySelector('.expanded').classList.add('nodisplay')
        }
    }
}

</script>




<!-- the "full" div is for desktop -->
<div class="full">
    <ul>
        <li><a href="/what-we-do" class="what-we-do">What We Do</a></li>
        <li><a href="/about" class="about">About Us</a></li>
        <li><a href="/projects" class="projects">Projects</a></li>
        <li><a href="/resources" class="resources">Resources</a></li>
        <li><a href="/events" class="events">Events</a></li>
        <li><div class="faIcon"><a href={raftrURL} target="_blank"><Fa icon={faOtter} /></a></div></li>
        <li><div class="faIcon"><a href={githubURL} target="_blank"><Fa icon={faGithub} /></a></div></li>
        <li><div class="faIcon"><a href={discordURL} target="_blank"><Fa icon={faDiscord} /></a></div></li>
        <li><div class="faIcon"><a href={instaURL} target="_blank"><Fa icon={faInstagram} /></a></div></li>
        <li><div class="faIcon"><a href={linkedInURL} target="_blank"><Fa icon={faLinkedin} /></a></div></li>
    </ul>
</div>

<!-- the "collapsed" div is for mobile, and is only a menu button -->
<div class="collapsed">
    <button on:click={toggle}><Fa icon={faBars} /></button>
</div>

<!-- the "expanded" div is for mobile, after the menu has been expanded -->
<div class="expanded nodisplay">
    <ul>
        <li><a href="/what-we-do" class="what-we-do">What We Do</a></li>
        <li><a href="/about" class="about">About Us</a></li>
        <li><a href="/projects" class="projects">Projects</a></li>
        <li><a href="/resources" class="resources">Resources</a></li>
        <li><a href="/events" class="events">Events</a></li>
        <span>
            <li><div class="faIcon"><a href={raftrURL} target="_blank"><Fa icon={faOtter} /></a></div></li>
            <li><div class="faIcon"><a href={githubURL} target="_blank"><Fa icon={faGithub} /></a></div></li>
            <li><div class="faIcon"><a href={discordURL} target="_blank"><Fa icon={faDiscord} /></a></div></li>
            <li><div class="faIcon"><a href={instaURL} target="_blank"><Fa icon={faInstagram} /></a></div></li>
            <li><div class="faIcon"><a href={linkedInURL} target="_blank"><Fa icon={faLinkedin} /></a></div></li>
        </span>
        
    </ul>
</div>
<style>
    .full > ul {
        display: flex;
        list-style-type: none;
        padding: 0;
        margin: 0;
    }

    .full > ul > li {
        padding-left: 1vh;
        padding-right: 1vh;
        /* center vertically */
        display: flex;
        align-items: center;
    }

    .full > ul > li > a {
        text-decoration: none;
        color: #555;
        font-size: 1.4vh;
        font-family: "Nunito";
    }

    .faIcon {
        font-size: 2.5vh;
    }

    .full > ul > li > .faIcon > a {
        color: #555;
    }

    .full {
        /* align right */
        position: absolute;
        right: 5vw;
    }

    .expanded > ul {
        display: flex;
        flex-direction: column;
        list-style-type: none;
        /* padding: 2vh; */
    }

    .expanded > ul > li {
        padding-top: 1vh;
        padding-bottom: 1vh;
    }

    .expanded > ul > li > a {
        text-decoration: none;
        color: #555;
        font-size: 2.5vh;
        font-family: "Nunito";
    }

    .expanded > ul > span {
        display: flex;
        justify-content: center;
    }

    .expanded > ul > span > li {
        padding-left: 1vh;
        padding-right: 1vh;
    }

    .expanded > ul > span > li > .faIcon > a {
        color: #555;
        font-size:7vh;
    }
    
    button {
        background-color: white;
        border: none;
        font-size: 2.5vh;
    }

    :global(.active){
        font-weight: 900;
    }
        
    /* if on desktop */
    @media screen and (orientation: landscape) { 

        
        .collapsed {
            display: none;
        }

        .expanded {
            display: none;
        }
    }

    /* if on mobile */
    @media screen and (orientation: portrait) {
        .full {
            display: none;
        }

        .collapsed {
            display: flex;
            justify-content: center;
            align-items: center;
            font-size: 2.5vh;
            position: absolute;
            right: 5vw;
            top: 0;
            height:7vh;
        }


        .nodisplay {
            display: none;
        }

        .expanded {
            margin-top:7vh;
            z-index:100;
            background-color: white;
            width:100%;
        }
    }
    
</style>



