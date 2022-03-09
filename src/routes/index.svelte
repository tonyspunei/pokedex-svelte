<script>
  import { pokemon } from "../stores/pokestore";
  import PokemanCard from "../components/pokemanCard.svelte";

  let searchTerm = "";
</script>

<svelte:head>
  <title>Svelte Kit Pokedex</title>
</svelte:head>

<h1 class="text-4xl text-center my-8 uppercase">Svelte Kit</h1>
<div class="grid gap-4 md:grid-cols-2 grid-cols-1 py-4">
  {#each $pokemon as pokeman}
    <PokemanCard pokeman="{pokeman}" />
  {/each}
</div>
