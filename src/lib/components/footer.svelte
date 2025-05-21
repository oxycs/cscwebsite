<script>
	import { emailAddr, emailPlaintext } from "../../constants";

</script>
<!-- this is the footer at the bottom of the page. -->
<!-- it is a flexbox row. You can copy and paste more columncontainers to add additional sections. -->



<footer>
    <div class="flexcontainer">
        <div class="columncontainer">
            <p>Computer Science Club</p>
            <a href="https://oxy.edu">Occidental College</a>
        </div>
        <div class="columncontainer">
            <p>1600 Campus Road</p>
            <p>Los Angeles, CA 90041</p>
            <a href={emailAddr}>{emailPlaintext}</a>
        </div>
    </div>
</footer>


<style>
    footer {
        background-color: rgb(45,46,46);
        color: #fff;
        width: 100%;
        position: absolute;
        left: 0px;
        min-height: 5vh;
        font-size:1.5vh;
        padding-bottom:1vh;
        font-family: "Nunito", sans-serif;
    }
    .flexcontainer {
        display: flex;
        justify-content: space-evenly;
        align-items: center;
        flex-direction: row;
        min-height: 5vh;
    }
    a {
        color:rgb(253, 115, 70);
        text-decoration: none;
    }
</style>