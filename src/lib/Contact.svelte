<script>
    import { fly } from "svelte/transition";
</script>

<div class="contact" in:fly={{ y: -30, duration: 400 }}>
    <h1>contact me</h1>
    <p>email: hi@xenon.zone</p>
    <p>discord: xenonorsomething</p>
</div>

<style>
    h1 {
        margin: 15px;
    }
    .contact {
        line-height: 5px;
    }
</style>
