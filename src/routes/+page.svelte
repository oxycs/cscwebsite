<script lang="ts">
    import Eventrow from "$lib/components/eventrow.svelte";
</script>
<title>Oxy Computer Science Club</title>
<div class="main">
    <div class="section one fullheight">
        <div class="title">
            <span class="whitetext"><p>Computer</p></span>
            <span class="orangetext"><p>Science</p></span>
            <span class="whitetext"><p>Club</p></span>
        </div>
        <a href="/what-we-do"><button>What We Do</button></a>
        <p class="whitetext">Our mission is to create an inclusive and collaborative community around Computer Science and provide resources and opportunities for all Oxy students.</p>
    </div>
    <div class="section two ">
        <div class="half">
            <h2>Your Voice in the CS Department</h2>
            <p>Make your voice heard in the Computer Science Department! We give feedback to them directly, helping to improve your learning experience.</p>
        </div>
        <div class="half rotleft">
            <img src="/img/omac.jpg" alt="oMac Lab">
        </div>
    </div>
    <div class="section two swapimg">
        <div class="half">
            <h2>Meet Other CS Students!</h2>
            <p>We organize Computer Science social events, so you can get to know others who share your interest. </p>
        </div>
        <div class="half rotright">
            <img src="/img/cscmeeting.png" alt="CS Club Meeting">
        </div>
    </div>
    <div class="section two">
        <div class="half">
            <h2>Talks and Panels</h2>
            <p>Attend our internship panel to hear about the experiences of others getting internships! You can also learn about important topics and tools like Git or Linux from our talks.</p>
        </div>
        <div class="half rotleft">
            <img src="/img/internpanel2.png" alt="Internship Panel">
        </div>
    </div>
    <div class="section three">
        <h2>Upcoming Events</h2>
        <Eventrow></Eventrow>
    </div>
    
</div>

<style>
    .main {
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
        font-family: "Nunito", sans-serif;
        width:100%;
    }

    .section {
        width: 100%;
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .fullheight {
        height: 93vh;
    }
    
    .one {
        background:linear-gradient(rgba(0, 0, 0, 0.5), rgba(0, 0, 0, 0.5)),url('/img/serverroom.png');        
        background-size: cover;
        background-repeat: no-repeat;
        background-attachment: fixed;
        background-position: center;
        flex-direction: column;
    }

    .two {
        flex-direction: row;
        padding-top:2vh;
        padding-bottom:2vh;
    }

    .swapimg {
        flex-direction: row-reverse;
    }

    .three {
        flex-direction: column;
        padding-top:2vh;
        padding-bottom:2vh;
        width:100%;
    }

    .three > h2 {
        font-size: 4vh;
    }

    .half {
        width: 50%;
        /* height: 50vh; */
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
        margin-left:5vw;
        margin-right:5vw;
    }

    .half > img {
        width: 100%;
        border-radius: 1vw;
        /* shadow */
        box-shadow: 10px 9px 14px 1px rgba(0,0,0,0.64);
    }

    .rotleft, .rotright {
        transition: 0.3s;
    }
    .rotleft:hover {
        transform: scale(1.05) rotateZ(-1deg);
    }
    .rotright:hover {
        transform: scale(1.05) rotateZ(1deg);
    }

    .title {
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
        font-size: 10vh;
    }

    .whitetext {
        color: white;
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

    /* MOBILE PORTRAIT MODE */
    @media screen and (orientation: portrait) {
        .swapimg {
            flex-direction: column;
        }
        .two {
            flex-direction: column;
        }

        .half {
            width: 90%;
        }
    }
</style>