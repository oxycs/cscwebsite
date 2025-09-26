<script>
	export let img = '/img/grafanathumb.jpg';
	export let imgalt = 'Placeholder Alt Text';
	export let title = 'Title';
	export let description = 'Description';
	export let url = 'https://example.com';
	import Fa from 'svelte-fa';
	import { faArrowRight } from '@fortawesome/free-solid-svg-icons';
</script>

<a href={url} target="_blank">
	<!-- <img class="projectimg" src={img} alt={imgalt} /> -->
	<div class="imgbg" style="background-image: url({img});"></div>
	<div class="projectinfo">
		<h2>{title}</h2>
		<p>{description}</p>
	</div>
	<div class="button">
		<Fa icon={faArrowRight} />
	</div>
</a>

<style>
	a {
		text-decoration: none;
		color: inherit;
		display: flex;
		justify-content: space-between;
		align-items: center;
		margin-top: 2vh;
		width: 80%;
		border: 1px solid #555;
		border-radius: 10px;
	}

	* {
		font-family: 'Nunito', sans-serif;
	}

	.imgbg {
		width: calc(173px * (16 / 9));
		height: 173px;
		background-size: calc(173px * (16 / 9)) auto;
		background-repeat: no-repeat;
		background-position: center;
	}

	@media screen and (orientation: portrait) {
		a {
			flex-direction: column;
		}

		.imgbg {
			max-width: 100%;
		}
	}

	@media screen and (orientation: landscape) {
		a {
			flex-direction: row;
		}

		.imgbg {
			border-radius: 9px 0px 0px 9px;
		}
	}

	.projectinfo {
		display: flex;
		justify-content: center;
		align-items: center;
		flex-direction: column;
		width: 50%;
		text-align: center;
		padding: 0.75em 2em;
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
		font-size: 4vh;
		color: #555;
		text-decoration: none;
		padding-bottom: 0.5em;
	}

	.button:hover {
		color: rgb(253, 115, 70);
	}
</style>
