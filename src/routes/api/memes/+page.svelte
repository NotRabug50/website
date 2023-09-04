<script>
    let memes = [];
    import {onMount} from "svelte";

    async function fetchMemes() {
      try {
        const response = await fetch("https://meme-api.com/gimme/1");
        const data = await response.json();
        memes = data.memes;
      } catch (error) {
        console.error("Veri çekme hatası:", error);
      }
    }
    
    onMount(() => {
      fetchMemes();
    });
  </script>
  
  {#if memes.length > 0}
    {#each memes as meme}
      <img src={meme.url} alt={meme.title} />
    {/each}
  {:else}
    <p>Loading...</p>
  {/if}
  
  <style>
    img {
      max-width: 100%;
      height: auto;
    }
  </style>
  