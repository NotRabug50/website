<script>
    // Define props or variables as needed
    export let navLinks = [];

    let titles = ["rabug", "NotRabug50", "TheRabug"];
    let currentTitleIndex = 0;
    let currentTitle = "";
    let isTyping = false;

    function startTypingEffect() {
        const targetTitle = titles[currentTitleIndex];
        let index = 0;

        function type() {
            if (index <= targetTitle.length) {
                currentTitle = targetTitle.substring(0, index);
                index++;
                setTimeout(type, 100); // Typing speed (milliseconds)
            } else if (index === targetTitle.length + 1) {
                setTimeout(erase, 3000); // Wait for 3 seconds after typing the title
                index++;
            }
        }

        function erase() {
            if (index >= 0) {
                currentTitle = targetTitle.substring(0, index);
                index--;
                setTimeout(erase, 100); // Erasing speed (milliseconds)
            } else {
                nextTitle();
            }
        }

        function nextTitle() {
            currentTitleIndex = (currentTitleIndex + 1) % titles.length;
            isTyping = false;
            startTypingEffect();
        }

        type();
    }

    // Trigger the typing effect when the component is mounted
    import { onMount } from "svelte";
    onMount(() => {
        startTypingEffect();
    });
</script>

<header>
    <title>{currentTitle}&#8203;</title>
    <div class="container">
        <h1>
            <a href="/" class="title">{currentTitle}&#8203;</a>
            <span class="cursor">_</span>
        </h1>
        <nav>
            <ul>
                {#each navLinks as link}
                <li><a href={link.url}>{link.text}</a></li>
                {/each}
            </ul>
        </nav>
    </div>
    <p style="font-size: 10px">website may look empty or unfinished</p>
</header>

<style>
    header {
        background-color: #222; /* Dark background color */
        color: #fff; /* Light text color */
        padding: 1rem 0;
        text-align: center;
    }

    .title {
        font-size: 2.5rem;
        color: #fff; /* White title color */
        text-decoration: none; /* Remove the default underline */
        overflow: hidden; /* Hide overflowing text */
        display: inline-block; /* Allow inline block for animation */
    }

    .cursor {
        animation: blink 1s step-end infinite;
    }

    @keyframes blink {
        50% {
            opacity: 0;
        }
    }

    nav ul {
        list-style: none;
    }

    nav li {
        display: inline;
        margin-right: 1rem;
    }

    nav a {
        color: #fff; /* White link color */
    }

    nav a:hover {
        text-decoration: none;
    }
</style>
