<script>
    let email = "rabug50@gmail.com";
    let discord = "https://discord.com/users/541194606214250496";
    let github = "https://github.com/NotRabug50";
  </script>
  
  <main>
    <h1>Contact Me</h1>
    <p>If you'd like to get in touch, you can reach me via email or connect with me on social media:</p>
  
    <ul class="contact-list">
      <li>
        <strong>Email:</strong> <a href={"mailto:" + email}>{email}</a>
      </li>
      <li>
        <strong>Discord:</strong> <a href={discord} target="_blank" rel="noopener noreferrer">therabug</a>
      </li>
      <li>
        <strong>GitHub:</strong> <a href={github} target="_blank" rel="noopener noreferrer">NotRabug50</a>
      </li>
    </ul>
  </main>
  
  <style>
    /* Add your CSS styles here for the Contact page */
    h1 {
      font-size: 2rem;
      margin-bottom: 1rem;
    }
  
    p {
      font-size: 1.1rem;
      line-height: 1.6;
      margin-bottom: 1rem;
    }
  
    ul.contact-list {
      list-style: none;
      padding: 0;
    }
  
    li {
      font-size: 1rem;
      margin-bottom: 0.5rem;
    }
  
    a {
      color: #007bff;
      text-decoration: none;
    }
  
    a:hover {
      text-decoration: underline;
    }
    
  </style>
  