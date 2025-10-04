<script>
    import { fly } from "svelte/transition";

    export let path = "";
</script>

<div class="notfound" in:fly={{ y: -30, duration: 400 }}>
    <h1>not found</h1>
    <p>the page you requested ({path}) does not exist</p>
    <a href="#home">[go home]</a>
</div>

<style>
    .notfound {
        text-align: center;
    }
    .notfound h1 {
        color: red;
    }
</style>
