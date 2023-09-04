<script>
    export let techStack;
  
    // You can define additional props or logic here
  </script>
  
  <div class="tech-stack">
    <h3>My Tech Stack</h3>
    <ul>
      {#each techStack as tech}
        <li class="tech-item">
          <img src={tech.icon} alt={tech.name} />
          <span>{tech.name}</span>
        </li>
      {/each}
    </ul>
  </div>
  
  <style>
    /* Add your CSS styles here for the TechStack component */
    .tech-stack {
      background-color: #f4f4f4;
      border: 1px solid #ddd;
      border-radius: 4px;
      padding: 1rem;
      text-align: left;
      max-width: 300px;
    }
  
    h3 {
      font-size: 1.5rem;
      margin-bottom: 0.5rem;
    }
  
    ul {
      list-style: none;
      padding: 0;
    }
  
    .tech-item {
      display: flex;
      align-items: center;
      margin-bottom: 0.5rem;
    }
  
    img {
      width: 24px; /* Adjust the icon size as needed */
      height: 24px;
      margin-right: 0.5rem;
    }
  </style>
  