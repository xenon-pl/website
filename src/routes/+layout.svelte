<script lang="ts">
	import './layout.css';

	let { children } = $props();
</script>

<svelte:head
	><link rel="icon" href="/sun.png" />
	<title>xenon.zone</title>
</svelte:head>
{@render children()}
