<script>
    // Define an array of blog posts (you can replace this with your actual blog data)
    let blogPosts = [
      {
        title: "Getting Started with Svelte",
        date: "September 15, 2023",
        content: `
          In this blog post, I'll introduce you to the amazing world of Svelte and 
          show you how to get started with this innovative JavaScript framework. 
          Svelte's approach to building web applications is both efficient and 
          intuitive, making it a game-changer in the frontend development landscape.
        `,
      },
      {
        title: "The Power of Server-Side Rendering (SSR)",
        date: "October 10, 2023",
        content: `
          Server-Side Rendering (SSR) is a crucial technique for improving web 
          application performance and SEO. In this post, I'll explain the benefits 
          of SSR and demonstrate how to implement it in your SvelteKit projects.
        `,
      },
      // Add more blog posts as needed
    ];
  </script>
  
  <main>
    <h1>My Tech Blog</h1>
  
    <ul class="blog-list">
      {#each blogPosts as post}
        <li class="blog-post">
          <h2>{post.title}</h2>
          <p class="date">{post.date}</p>
          <p>{post.content}</p>
        </li>
      {/each}
    </ul>
  </main>
  
  <style>
    /* Add your CSS styles here for the Blogs page */
    h1 {
      font-size: 2rem;
      margin-bottom: 1rem;
    }
  
    ul.blog-list {
      list-style: none;
      padding: 0;
    }
  
    .blog-post {
      margin-bottom: 2rem;
    }
  
    h2 {
      font-size: 1.5rem;
      margin-bottom: 0.5rem;
    }
  
    .date {
      color: #777;
      font-size: 1rem;
      margin-bottom: 0.5rem;
    }
  
    p {
      font-size: 1.1rem;
      line-height: 1.6;
    }
  </style>
  
