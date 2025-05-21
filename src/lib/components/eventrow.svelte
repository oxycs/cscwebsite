
<script lang="ts">
    import Event from "$lib/components/event.svelte";
    import { icalJSON } from "../../constants";




    async function loadEvents() {
        let res = await fetch(icalJSON);
        const data = await res.json();

        for (let i = 0; i < data.VCALENDAR[0].VEVENT.length; i++){
            let date;
            if (data.VCALENDAR[0].VEVENT[i]["DTSTART;TZID=America/Los_Angeles"]){
                date = data.VCALENDAR[0].VEVENT[i]["DTSTART;TZID=America/Los_Angeles"];
            } else {
                date = data.VCALENDAR[0].VEVENT[i]["DTSTART"];
            }
            data.VCALENDAR[0].VEVENT[i].PROPERDT = new Date(date.slice(0,4) + "-" + date.slice(4,6) + "-" + date.slice(6,8) + "T" + date.slice(9,11) + ":" + date.slice(11,13) + ":" + date.slice(13,15) + "Z");
        }
        

        // data.VCALENDAR[0].VEVENT.reverse();
        // sort calendar by PROPERDT
        data.VCALENDAR[0].VEVENT.sort((a, b) => {
            return a.PROPERDT - b.PROPERDT;
        });

        return data.VCALENDAR[0].VEVENT.reverse();
    }

</script>






<div class="eventrow">
    {#await loadEvents()}
	<p>waiting for the events to load...</p>
    {:then value}
        {#each value as event}
            <Event title={event.SUMMARY} date={event.PROPERDT.toDateString()} location={event.LOCATION} description={event.DESCRIPTION}></Event>
        {/each}
    {:catch error}
        <p>There was an error loading the events</p>
    {/await}
</div>


<style>
    .eventrow {
        width:100%;
        overflow:scroll;
        white-space: nowrap;
        flex-direction: row;
        scrollbar-width: none;
        padding-bottom: 1vh;
    }
</style>