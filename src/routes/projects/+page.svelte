<script lang="ts">
    import Fa from 'svelte-fa'
    import { faArrowRight } from '@fortawesome/free-solid-svg-icons'
    </script>
    
    <div class="heading">
        <h1>Projects</h1>
        <p>A directory of student works, hosted by the Computer Science Club</p>
    </div>
    
    <div class="projectlist">
        <div class="project">
            <img class="projectimg" src="/img/grafanathumb.jpg" alt="Grafana Graph Thumbnail">
            <div class="projectinfo">
                <h2>Dining Busyness Graph</h2>
                <p>A live chart displaying how busy each dining area on campus is.</p>
            </div>
            <div class="button">
                <a href="https://dining.csc.oxy.edu" target="_blank"><Fa icon={faArrowRight} /></a>
            </div>
        </div>
        <div class="project">
            <img class="projectimg" src="/img/quacs_logo.svg" alt="QuACS Logo">
            <div class="projectinfo">
                <h2>QuACS OXY</h2>
                <p>Questionably Accurate Course Scheduler for Occidental College</p>
            </div>
            <div class="button">
                <a href="https://quacs.nicholasnovak.io" target="_blank"><Fa icon={faArrowRight} /></a>
            </div>
        </div>
    </div>
    
    <style>
        * {
            font-family: "Nunito", sans-serif;
        }
    
        .heading {
            display: flex;
            justify-content: center;
            align-items: center;
            flex-direction: column;
            font-size: 2.5vh;
            margin-top: 5vh;
        }
    
        .projectlist {
            display: flex;
            justify-content: center;
            align-items: center;
            flex-direction: column;
            margin-top: 5vh;
        }
    
        .project {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-top: 2vh;
            width: 80%;
            border: 1px solid #555;
            border-radius: 10px;
        }
    
        @media screen and (orientation: portrait) {
            .project {
                flex-direction: column;
            }
    
            .projectimg {
                border-radius: 10px;
            }
        }
    
        @media screen and (orientation: landscape) {
            .project {
                flex-direction: row;
            }
    
            .projectimg {
                border-radius: 10px 0px 0px 10px;
            }
        }
    
        .projectimg {
            height: 20vh;
            max-width: 40vh;
            object-fit: contain;
        }
    
        .projectinfo {
            display: flex;
            justify-content: center;
            align-items: center;
            flex-direction: column;
            width: 50%;
        }
    
        .projectinfo > h2 {
            font-size: 2.5vh;
            margin: 0;
        }
    
        .projectinfo > p {
            font-size: 2vh;
            margin: 0;
        }
    
        .button {
            display: flex;
            justify-content: center;
            align-items: center;
            width: 20%;
        }
    
        .button > a {
            font-size: 4vh;
            color: #555;
            text-decoration: none;
        }
    
        .button > a:hover {
            color: rgb(253, 115, 70);
        }
    
    </style>