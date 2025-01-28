<script>
    export let title = "Title";
    export let date;
    export let location = "";
    export let description = "";
    let soon = "";
    // let soon = "In 5 days";
    let eventDate = new Date(date);
    let now = new Date();
    let diff = eventDate - now;
    let days = Math.floor(diff / (1000 * 60 * 60 * 24));
    if (days > 0){
        soon = "In " + days + " days";
    } else if (days == 0){
        soon = "Today";
    } else {
        soon = "In the past";
    }
    // replace \n with <br> for newlines
    description = description.replaceAll("\\n", "<br>").replaceAll("\\", "");
    location = location.replaceAll("\\n", "").replaceAll("\\", "");
    title = title.replaceAll("\\n", "").replaceAll("\\", "");

  </script>

<div class="box">
    <!-- slot is the content of the page -->
    <p class="soon">{soon}</p>
    <h3>{title}</h3>
    {#if date}
    <p><b>Date: </b>{date}</p>
    {/if}
    {#if location}
    <p><b>Location: </b>{location}</p>
    {/if}
    <p>{@html description}</p>
</div>

<style>
    .box {
        display:inline-block;
        border-radius: 1vh;
        border: 1px solid #ccc;
        padding: 2vh;
        margin: 2vh;
        width:70vw;
        height:40vh;
        box-shadow: 10px 9px 14px 1px rgba(0,0,0,0.5);
        white-space: normal;
        /* overflow should scroll down */
        overflow-y: auto;
    }

    h3 {
        font-size: 30px;
        margin-top: 0px;
        margin-bottom: 0px;
    }

    p {
        font-size: 20px;
        margin:10px;
        margin-left:0px;
        margin-right:0px;
    }

    .soon {
        font-size: 18px;
        color: dodgerblue;
        margin:0px;
    }
    
</style>