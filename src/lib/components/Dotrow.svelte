<script lang="ts">
  // TODO: fix this mess, i way overcomplicated this
  // also way too much unused shit cuz the idea for this changed like 5 times midway through making ittt
  // in conclusion, this is sit

  import Dot from "$lib/components/Dot.svelte";

  interface DotDef {
    xOff: number;
    yOff: number;
    size: number;
    opacity: number;
    offset: number;
  }

  // shit
  let DotAmount = 250;

  let Dots: DotDef[] = [];
  let offset = 0;
  for (let i = 0; i < DotAmount; i++) {
    offset++;
    let size = Math.floor(5 + Math.random() * 2);
    let opacity = Math.floor(60 + Math.random() * 40);

    Dots.push({
      xOff: 0,
      yOff: 0,
      size: size,
      opacity: opacity,
      offset: offset,
    } as DotDef);
  }
</script>

<div class="dotrow flex items-center gap-2 align-middle">
  {#each Dots as dot}
    <Dot opacity={dot.opacity} offset={dot.offset} />
  {/each}
</div>
