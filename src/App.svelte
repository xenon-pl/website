<script lang="ts">
    import svelteLogo from "./assets/svelte.svg";
    import viteLogo from "/vite.svg";
    import Counter from "./lib/Counter.svelte";
</script>

<main>
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
    <!---
	    <h2>Projects</h2>
    <div class="links">
        <a href="https://github.com/xenon-pl" class="button"> GitHub </a>
        <a href="https://github.com/xenon-pl" class="button"> YouTube </a>
        <a href="https://github.com/xenon-pl" class="button"> Steam </a>

        <a href="https://github.com/xenon-pl" class="button"> Discord </a>
    </div>
	-->
    <!--
    <p>--------------------------</p>
    <p>my projects:</p>
    <div class="links">
        <p class="button notclickable">Talon</p>
        <p class="button notclickable">Taurine</p>
        <p class="button notclickable">Tsikuni</p>
        <p class="button notclickable">Furequency</p>
    </div>
    <p class="subtext">damn, im not good at finishing projects</p>
    -->
</main>

<style>
    a {
        text-decoration: underline;
        font-size: medium;
    }
    .spacer {
        padding: 5px;
    }
    h1 {
        font-size: 50px;
        font-family: "VT323", monospace;
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
    .button {
        background-color: white;
        color: black;
        font-size: large;
        padding: 5px 15px;
        margin: 5px;
        transition: 0.1s ease-in-out;
    }
    .notclickable {
        background-color: black;
        color: white;
        outline: 1px solid white;
        flex-wrap: wrap;
    }
    .button:hover {
        transform: translateY(-5px);
    }
    .cat {
        margin: 0;
        scale: 250%;
    }
    .subtext {
        color: rgb(13, 13, 13);
    }
    .bio {
        line-height: normal;
        margin-top: 0;
    }
    .name {
        margin-bottom: 0;
    }
</style>
