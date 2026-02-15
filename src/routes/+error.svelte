<!-- took this from the tsikuni website, which isnt tailwind so theres just regular css here -->

<script lang="ts">
	// niko!
	const niko = '/niko.png';
	const nikomouseover = '/nikomouseover.png';

	let nikoElement!: HTMLImageElement;

	function NikoMouseOver() {
		nikoElement.src = nikomouseover;
	}

	function NikoMouseOut() {
		nikoElement.src = niko;
	}
</script>

<svelte:head>
	<title>not found</title>
	<meta
		name="description"
		content="the page you're looking for no longer exists, or another error occured."
	/>
</svelte:head>

<div class="theworldmachine">
	<h1>404</h1>
	<p>the page you're looking for no longer exists</p>
</div>
<!-- svelte-ignore a11y-mouse-events-have-key-events -->
<button class="nikobutton" onmouseover={NikoMouseOver} onmouseout={NikoMouseOut}>
	<img src={niko} alt="niko" class="niko" title="niko" bind:this={nikoElement} />
</button>

<style>
	.theworldmachine {
		position: absolute;
		top: 0;
		bottom: 0;
		left: 0;
		right: 0;
		justify-content: center;
		justify-self: center;
		align-items: center;
		align-content: center;
		text-align: center;
		font-size: xx-large;
	}
	p {
		margin: 0;
	}
	h1 {
		margin: 0;
	}

	.nikobutton {
		position: absolute;
		bottom: 25px;
		left: 0;
		right: 0;
		text-align: center;
		cursor: pointer;
		background: transparent;
		border: 0px solid transparent;
		outline: 0px solid transparent;
		width: fit-content;
		height: fit-content;
	}
</style>
