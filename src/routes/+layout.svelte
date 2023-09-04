<script>
    // Import the Header component
    import Header from "./Header.svelte";
    import './styles.css'
    import {onMount} from "svelte";
    // Define the navigation links for the header
    let navLinks = [
      { url: "/", text: "home" },
      { url: "/projects", text: "projects" },
      { url: "/about", text: "about" },
      { url: "/contact", text: "contact" },
      { url: "/blog", text: "blog" },
      { url: "/login", text: "login" }
    ];
    // Define an array of emojis to choose from
    const emojis = ["😃", "🚀", "👍", "💻", "🌟", "🎉", "🔥", "❤️"];
  
    // Function to randomly select an emoji from the array
    function getRandomEmoji() {
      const randomIndex = Math.floor(Math.random() * emojis.length);
      return emojis[randomIndex];
    }
  
    // Initialize the emoji with a random selection
    let randomEmoji = "";
    let isMounted = false;

    onMount(() => {
        randomEmoji = getRandomEmoji();
        isMounted = true
    });

    import { fly } from 'svelte/transition';

    export let data;
  </script>
 
  <div>
    <Header title="rabug" {navLinks} />
  
    {#key data.url}
    <div
      in:fly={{ x: 0, duration: 300, delay: 300 }}
      out:fly={{ x: 0, duration: 300 }}>
      <slot />
      </div>
      {/key}
  </div>

    <div class="container", style="padding: 1rem 0; margin: 0 auto; text-align: center;">
      <p>{randomEmoji}</p>
    </div> 

  <style>
    .container {
      max-width: 1200px;
      margin: 0 auto;
      padding: 1rem;
    }
  </style>
  