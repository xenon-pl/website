<script>
    import { fly } from "svelte/transition";
</script>

<div class="titlebar" in:fly={{ y: -30, duration: 400 }}>
    <div class="section">
        <h1 class="cat">🦌</h1>
        <div class="spacer"></div>
        <h1 class="name">xenon.zone</h1>
    </div>
    <div class="section">
        <a href="#home">[Home]</a>
        <a href="#about">[About Me]</a>
        <a href="#stuff">[My Stuff]</a>
        <a href="#contact">[Contact Me]</a>
    </div>
</div>

<style>
    .titlebar {
        position: fixed;
        top: 15px;
        left: 15px;
        right: 15px;
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 10px;
        background-color: #000000;
        outline: 2px solid white;
        line-height: 0;
        height: 30px;
    }
    .section {
        display: flex;
        align-items: center;
    }
    .name {
        margin: 0;
        font-size: 1.5em;
    }
    .spacer {
        padding: 5px;
    }
    a {
        text-decoration: underline;
        font-size: medium;
        margin-left: 15px;
        font-size: clamp(10px, 2.5vw, 16px);
        text-overflow: ellipsis;
        text-wrap: ellipsis;
    }
    .cat {
        font-family: "Noto Emoji";
        font-size: 1.75em;
        margin: 0;
    }
    @media (max-width: 600px) {
        .name {
            display: none;
        }
    }
</style>
