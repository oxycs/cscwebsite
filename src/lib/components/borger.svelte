<script lang="ts">
import Fa from 'svelte-fa'
import { faBars, faS } from '@fortawesome/free-solid-svg-icons'
import { faSlack, faGithub, faFacebook, faInstagram } from '@fortawesome/free-brands-svg-icons'
import { onMount } from 'svelte'

let expanded = false
let loaded = false

// wait for onMount to finish before running toggle
onMount(() => {
    loaded = true
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





<div class="full">
    <ul>
        <li><a href="/what-we-do">What We Do</a></li>
        <li><a href="/about">About Us</a></li>
        <li><a href="/resources">Resources</a></li>
        <li><a href="/events">Events</a></li>
        <li><div class="faIcon"><a href="https://example.com"><Fa icon={faSlack} /></a></div></li>
        <li><div class="faIcon"><a href="https://example.com"><Fa icon={faGithub} /></a></div></li>
        <li><div class="faIcon"><a href="https://example.com"><Fa icon={faFacebook} /></a></div></li>
        <li><div class="faIcon"><a href="https://example.com"><Fa icon={faInstagram} /></a></div></li>
    </ul>
</div>
<div class="collapsed">
    <button on:click={toggle}><Fa icon={faBars} /></button>
</div>
<div class="expanded nodisplay">
    <ul>
        <li><a href="/what-we-do">What We Do</a></li>
        <li><a href="/about">About Us</a></li>
        <li><a href="/resources">Resources</a></li>
        <li><a href="/events">Events</a></li>
        <span>
            <li><div class="faIcon"><a href="https://example.com"><Fa icon={faSlack} /></a></div></li>
            <li><div class="faIcon"><a href="https://example.com"><Fa icon={faGithub} /></a></div></li>
            <li><div class="faIcon"><a href="https://example.com"><Fa icon={faFacebook} /></a></div></li>
            <li><div class="faIcon"><a href="https://example.com"><Fa icon={faInstagram} /></a></div></li>
        </span>
        
    </ul>
</div>

<style>
    /* display full > ul > li in a line */
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
        font-size: 1vh;
        font-family: "Nunito";
    }

    .faIcon {
        font-size: 1.8vh;
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
        font-size:5vh;
    }
    
    button {
        background-color: white;
        border: none;
        font-size: 2.5vh;
    }

    @media screen and (orientation: landscape) {
        .collapsed {
            display: none;
        }

        .expanded {
            display: none;
        }
    }
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
            height:5vh;
        }


        .nodisplay {
            display: none;
        }

        .expanded {
            margin-top:5vh;
            z-index:100;
            background-color: white;
            width:100%;
        }
    }
    
</style>



