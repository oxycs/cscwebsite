<script>
    export let title = "Title";
    export let date = "Date";
    export let location = "";
    export let description = "Description";
  </script>

<div class="box">
    <!-- slot is the content of the page -->
    <h3>{title}</h3>
    <p><b>Date: </b>{date}</p>
    <p><b>Location: </b>{location}</p>
    <p>{description}</p>
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
    }

    h3 {
        font-size: 30px;
    }

    p {
        font-size: 20px;
    }
    
</style>