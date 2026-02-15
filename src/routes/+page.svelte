<script lang="ts">
	import Bg from '$lib/components/Bg.svelte';
	import { onMount } from 'svelte';

	let player!: HTMLParagraphElement;

	onMount(() => {
		async function updateSong() {
			const res = await fetch('https://nowplaying.xenon.zone');
			const data = await res.json();

			if (data.now_playing) {
				player.textContent = `♫ now playing: ${data.track}`;
				player.title = `♫ now playing: ${data.track} by ${data.artist}`;
			} else {
				player.textContent = `last played: ${data.track} by ${data.artist}`;
			}
		}

		updateSong();
		setInterval(updateSong, 10000);
	});
</script>

<Bg />
<div class="absolute top-0 right-0 bottom-0 left-0 flex flex-col items-center justify-center">
	<div class="div text-7xl">🦌</div>
	<div class="header text-4xl font-bold">hi, im niko!</div>
	<p class="text-xl">i like to make fun, useful software.</p>
	<div class="m-2 flex">
		<!--svelte-ignore a11y_click_events_have_key_events-->
		<i
			class="fa-brands fa-youtube cursor-pointer gap-2 text-3xl transition-[0.3s_ease] hover:scale-110"
			role="button"
			tabindex="0"
			onclick={() => {
				window.open('https://www.youtube.com/channel/UCIMNqUjrmXPZHcOh9Q77nLA');
			}}
		></i>
		<!--svelte-ignore a11y_click_events_have_key_events-->
		<i
			class="fa-brands fa-steam cursor-pointer text-3xl transition-[0.3s_ease] hover:scale-110"
			role="button"
			tabindex="0"
			onclick={() => {
				window.open('https://steamcommunity.com/id/-talons-/');
			}}
		></i>
		<!--svelte-ignore a11y_click_events_have_key_events-->
		<i
			class="fa-brands fa-discord cursor-pointer text-3xl transition-[0.3s_ease] hover:scale-110"
			role="button"
			tabindex="0"
			onclick={() => {
				window.open('https://discord.com/users/1147914900086206572');
			}}
		></i>
		<!--svelte-ignore a11y_click_events_have_key_events-->
		<i
			class="fa-brands fa-github cursor-pointer text-3xl transition-[0.3s_ease] hover:scale-110"
			role="button"
			tabindex="0"
			onclick={() => {
				window.open('https://github.com/xenon-pl');
			}}
		></i>
	</div>
	<p class="mt-4" bind:this={player}>now playing: [loading]</p>
</div>
