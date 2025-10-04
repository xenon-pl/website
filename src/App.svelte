<script lang="ts">
    import NotFound from "./lib/404.svelte";
    import Titlebar from "./lib/Titlebar.svelte";
    import Home from "./lib/Home.svelte";
    import About from "./lib/About.svelte";
    import Stuff from "./lib/Stuff.svelte";
    import Contact from "./lib/Contact.svelte";

    import { onMount } from "svelte";

    let section = window.location.hash || "#home";

    function doshit() {
        section = window.location.hash || "#home";
    }

    onMount(() => {
        window.addEventListener("hashchange", doshit);
        return () => window.removeEventListener("hashchange", doshit);
    });

    let path = typeof window !== "undefined" ? window.location.pathname : "/";
</script>

<Titlebar />
{#if section === "#home"}
    <Home />
{:else if section === "#about"}
    <About />
{:else if section === "#stuff"}
    <Stuff />
{:else if section === "#contact"}
    <Contact />
{:else}
    <NotFound {path} />
{/if}
