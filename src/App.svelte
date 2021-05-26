<script>
  import { onMount } from "svelte";
  export let collection;

  onMount(async () => {
    const res = await fetch("https://strong-traveling-panther.glitch.me//");
    const response = await res.json();
    collection = response.data;
  });
</script>

<main>
  <h1>CRM de Algo, para Software 3 ...</h1>

  <h2>The date according to Node.js is:</h2>
  <p>{collection ? collection?.productName : "Loading date..."}</p>
</main>
