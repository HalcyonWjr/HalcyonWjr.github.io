<script>
    export let title = "Default Project Title";
    export let date = "Project Date";
    export let description = "Project Description";
    export let imageUrl = "/default-image.png";
    export let projectUrl = "";
  </script>
  
  <div class="project-container">
    <div class="project-photo">
      <img src={imageUrl} alt="thumbnail">
    </div>
  
    <div class="project-text">
      <p class="project-title">{title}</p>        
      <p class="project-date">{date}</p>
      <p class="project-des">{description}</p>
      {#if projectUrl}
      <a href={projectUrl} target="_blank" class="project-link">[view online]</a>
      {/if}
    </div>
  </div>
  

  <style>
    .project-container {
      display: flex; 
      align-items: center; 
      gap: 20px; 
      margin-bottom: 40px;
    }

    .project-photo {
      flex-shrink: 0; 
    }

    .project-photo img {
      width: 100%; 
      height: 150px; 
      border: 1px solid black;
    }

    .project-text {
      margin: 10px
    }

    .project-title {
      font-size: 1.05rem;
      font-weight: 500;
      margin-bottom: 8px;
    }
    
    .project-date {
      font-weight: 300;
      color: grey;
    }

    .project-link {
      color: black;
      text-decoration: none;
      margin-right: 5px;
    }
    
    .project-link:hover {
      color: #509A23;
      text-decoration: underline;
    }
  </style>