<script>
    import { fly } from "svelte/transition";
</script>

<div class="stuff" in:fly={{ y: -30, duration: 400 }}>
    <h1>my projects</h1>
    <a href="https://tsikuni.lol/">[tsikuni]</a>
    <a href="https://github.com/xenon-pl/colourflies">[colourflies]</a>
    <a href="https://github.com/xenon-pl/taurine">[taurine]</a>
    <a href="https://github.com/xenon-pl/website">[this website!]</a>
    <h1>phones i own</h1>
    <a href="https://en.wikipedia.org/wiki/Pixel_8a">[pixel 8a (main)]</a>
    <a href="https://en.wikipedia.org/wiki/HTC_HD2">[htc leo]</a>
    <a href="https://en.wikipedia.org/wiki/IPhone_3GS">[iphone 3gs]</a>
    <a href="https://en.wikipedia.org/wiki/IPhone_11">[iphone 11]</a>
    <a href="https://en.wikipedia.org/wiki/IPhone_7">[iphone 7 plus]</a>
    <a href="https://en.wikipedia.org/wiki/Huawei_P30">[huawei p30 lite]</a>
    <a href="#stuff">[some xperia phone]</a>
</div>

<style>
    h1 {
        margin: 15px;
    }
    a {
        text-decoration: underline;
    }
</style>
