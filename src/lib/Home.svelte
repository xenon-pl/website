<script>
    import { fly } from "svelte/transition";
</script>

<div class="main" in:fly={{ y: -30, duration: 400 }}>
    <div class="thingy">
        <h1 class="cat">𓃠</h1>
        <h1 class="name">xenon.zone</h1>
        <p class="bio">
            i'm a polish teenager living in scotland.<br />VR Enthusiast,
            Developer, Artist and Producer
        </p>
    </div>
    <div class="links">
        <a href="https://github.com/xenon-pl"> [GitHub] </a>
        <div class="spacer"></div>
        <a href="https://www.youtube.com/channel/UCIMNqUjrmXPZHcOh9Q77nLA">
            [YouTube]
        </a>
        <div class="spacer"></div>
        <a href="https://steamcommunity.com/id/-talons-/"> [Steam] </a>
        <div class="spacer"></div>
        <a href="https://discord.com/users/1147914900086206572"> [Discord] </a>
    </div>
</div>

<style>
    a {
        text-decoration: underline;
        font-size: medium;
    }
    .spacer {
        padding: 5px;
    }
    .thingy {
        font-size: large;
        line-height: 0;
    }
    .links {
        display: flex;
        margin: auto;
        align-self: center;
        justify-content: center;
    }
    .cat {
        margin: 0;
        scale: 250%;
    }
    .bio {
        line-height: normal;
        margin-top: 0;
        font-size: clamp(14px, 2.5vw, 18px);
    }
    .name {
        margin-bottom: 0;
    }
    .main {
        z-index: -1;
    }
</style>
