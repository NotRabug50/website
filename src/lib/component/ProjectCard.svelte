<script>
    export let project;
  
    // You can define additional props or logic here
  </script>
  
  <div class="project-card">
    <div class="card-header">
      <h3>{project.title}</h3>
    </div>
    <div class="card-content">
      <p>{project.description}</p>
    </div>
    <div class="card-footer">
      <a href={project.link} target="_blank" rel="noopener noreferrer">View on GitHub</a>
    </div>
  </div>
  
  <style>
    /* Add your CSS styles here for the ProjectCard component */
    .project-card {
      background-color: #1f1f1f; /* Card background color */
      border-radius: 8px; /* Card border radius */
      overflow: hidden;
      max-width: 300px;
      margin: 0 auto;
      transition: transform 0.2s; /* Add a smooth hover effect */
      position: relative; /* Position for shadow */
      animation: rainbowShadow 3s linear infinite;
    }
  
    .project-card:hover {
      transform: translateY(-5px); /* Lift the card slightly on hover */
    }

    @keyframes rainbowShadow {
      0% {
        box-shadow: 0 0 5px rgba(255, 0, 0, 0.5), 0 0 15px rgba(255, 0, 0, 0.5), 0 0 30px rgba(255, 0, 0, 0.5);
      }
      25% {
        box-shadow: 0 0 5px rgba(255, 174, 0, 0.5), 0 0 15px rgba(255, 174, 0, 0.5), 0 0 30px rgba(255, 174, 0, 0.5);
      }
      50% {
        box-shadow: 0 0 5px rgba(0, 255, 13, 0.5), 0 0 15px rgba(0, 255, 13, 0.5), 0 0 30px rgba(0, 255, 13, 0.5);
      }
      75% {
        box-shadow: 0 0 5px rgba(4, 0, 255, 0.5), 0 0 15px rgba(4, 0, 255, 0.5), 0 0 30px rgba(4, 0, 255, 0.5);
      }
      100% {
        box-shadow: 0 0 5px rgba(255, 0, 0, 0.5), 0 0 15px rgba(255, 0, 0, 0.5), 0 0 30px rgba(255, 0, 0, 0.5);
      }
    }
  
    .card-header {
      background-color: #131313; /* Header background color */
      color: #fff; /* Header text color */
      padding: 1rem;
      text-align: center;
      border-radius: 10px;
    }
  
    .card-header h3 {
      margin: 0;
      font-size: 1.5rem; /* Header text size */
    }
  
    .card-content {
      padding: 1rem;
    }
  
    .card-content p {
      margin: 0;
      font-size: 1rem; /* Content text size */
    }
  
    .card-footer {
      background-color: #3a3a3a; /* Footer background color */
      padding: 1rem;
      text-align: center;
      border-radius: 10px;
    }
  </style>
  
  
  