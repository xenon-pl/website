<script>
    import { fly } from "svelte/transition";
</script>

<div class="about" in:fly={{ y: -30, duration: 400 }}>
    <div class="terminal">
        <h1>hey!</h1>
        <p>
            my name is xenon. i am a teenager from poland who lives in scotland
        </p>
        <br />
        <p>
            i generally like doing shit with technology. i also like music,
            football, art, VR, gaming, etc.
        </p>
        <br />
        <p>
            i grew up using computers a lot and it evolved into a love for
            programming, building shit, etc
        </p>
        <br />
        <p>
            i started programming when i was 9 or 10. it started as wanting to
            make a game and it ended up in me making websites, apps, etc
        </p>
    </div>
</div>

<style>
    .terminal {
        outline: 2px solid white;
        max-width: 600px;
        padding: 25px;
        text-align: left;
    }
    .about {
        text-align: center;
        z-index: 1;
    }
    .about h1 {
        margin-bottom: 0;
        margin: 0;
    }
    p {
        margin: 0;
    }
</style>
