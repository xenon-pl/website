<script lang="ts">
	import { onMount, onDestroy } from 'svelte';

	let dot: HTMLDivElement;
	export let opacity = 100;
	export let offset = 0;

	let i = offset * 0.1;
	let frame: number;

	function anim() {
		const y = Math.sin(i) * 50;
		const x = Math.sin(i) * 25;

		i += 0.01;

		dot.style.transform = `translate3d(${x}px, ${y}px, 0)`;

		frame = requestAnimationFrame(anim);
	}

	onMount(() => {
		dot.style.opacity = `${opacity / 100}`;
		frame = requestAnimationFrame(anim);
	});
</script>

<div
	class="h-2 w-2 max-w-2 min-w-2 rounded-full bg-foreground"
	style="will-change: transform;"
	bind:this={dot}
></div>
