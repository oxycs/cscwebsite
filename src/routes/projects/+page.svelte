<script lang="ts">
    import Arrowitem from '$lib/components/arrowitem.svelte';
    </script>
    
    <div class="heading">
        <h1>Projects</h1>
        <p>A directory of student works, hosted by the Computer Science Club</p>
    </div>
    
    <div class="projectlist">
        <Arrowitem img="/img/grafanathumb.jpg" imgalt="Grafana Graph Thumbnail" title="Dining Busyness Graph" description="A live chart displaying how busy each dining area on campus is." url="https://dining.csc.oxy.edu"></Arrowitem>
        <Arrowitem img="/img/quacs_logo.svg" imgalt="QuACS Screenshot" title="QuACS OXY" description="A course scheduling tool for Occidental College." url="https://quacs.nicholasnovak.io"></Arrowitem>
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
    
    </style>