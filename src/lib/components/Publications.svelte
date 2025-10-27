<script>
  import { onMount } from 'svelte';
  import SectionTitle from './SectionTitle.svelte';

  let publications = [];

  onMount(async () => {
      try {
          const response = await fetch('/publications.json');
          if (response.ok) {
              publications = await response.json();
          } else {
              console.error('Failed to fetch publications:', response.statusText);
          }
      } catch (error) {
          console.error('Error fetching publications:', error);
      }
  });
</script>

<section id="publications">
  <SectionTitle title="Publications" />

  {#if publications.length > 0}
      {#each publications as publication}
          <div class="publication-wrapper">
              <a
                class="paper-title"
                href={publication.links.publisher}
                target="_blank"
                rel="noopener noreferrer"
              >
                {publication.title}
              </a>
              
              <!-- <p class="author-list">
                {#each publication.authors.split(', ') as author, index (author)}
                  {#if author === 'Jinrui Wang'}
                    <span class="author-emphasis">{author}</span>
                  {:else}
                    {author}
                  {/if}
                  {#if index < publication.authors.split(', ').length - 1}<span>, </span>{/if}
                {/each}
              </p> -->
            
              <div class="source">
                  <p>
                    {#each publication.authors.split(',').map(a => a.trim()) as author, index (author)}
                      {#if author === 'Jinrui Wang'}
                        <span class="author-emphasis">{author}</span>{index < publication.authors.split(',').length - 1 ? ', ' : ''}
                      {:else}
                        {author}{index < publication.authors.split(',').length - 1 ? ', ' : ''}
                      {/if}
                    {/each}
                    .

                    <!-- <span class="conference-name">{publication.conference.name}</span> -->
                    <span style="font-style: italic;">{publication.conference.event}</span> 
                    {publication.conference.location}
                    ({publication.conference.year}).
                    {#if publication.conference.type}
                        <span class="paper-type"> ({publication.conference.type})</span>
                    {/if}

                    <span class="paper-honor">{publication.honor}</span>

                  </p>
              </div>


              <div>
                  {#if publication.links.paper}
                      <a class="paper-link" href={publication.links.paper} target="_blank">[ paper ]</a>
                  {/if}
                  {#if publication.links.github}
                      <a class="paper-link" href={publication.links.github} target="_blank">[ github ]</a>
                  {/if}
                  {#if publication.links.demo}
                      <a class="paper-link" href={publication.links.demo} target="_blank">[ live demo ]</a>
                  {/if}
                  {#if publication.links.website}
                      <a class="paper-link" href={publication.links.website} target="_blank">[ website ]</a>
                  {/if}
              </div>
          </div>
      {/each}
  {:else}
      <p>Loading publications...</p>
  {/if}
</section>

  
  <style>
    #publications {
      font-size: 1rem;
      line-height: 1.2rem;
    }

    .publication-wrapper {
      margin-bottom: 30px;
    }

    .source {
      display: flex;
      flex-wrap: wrap; 
      gap: 10px; 
      text-align: left;
      align-items: center;
    }

    .source p {
      margin: 2px 0;
      align-items: center;
      flex-wrap: wrap;
      font-weight: 300;
      font-size: 0.9rem;
      line-height: 1.2rem;
    }

    .paper-title{
      font-weight: 600;
      /* font-size: 1rem; */
      /* line-height: 1.2rem; */
      color: #396f18;
      /* color: black; */
      text-decoration: none;
    }

    .paper-title:hover {
      color: #509A23; 
      text-shadow: 2px 2px 6px rgba(80, 154, 35, 0.3);
      cursor: pointer;
    }

    .author-list {
      margin: 4px 0;
      font-size: 0.9rem;
      line-height: 1.1rem;
    }

    .author-emphasis {
      font-weight: 600;
      text-decoration: underline;
      text-decoration-style:wavy;
    }

    .conference-name {
      border: 1px solid #509A23; 
      border-radius: 5px; 
      padding: 2px 4px;
      margin-right: 5px;
      font-size: 0.75rem;
      font-weight: 400;
      align-items: center;
      height: 100%;  
    }

    .paper-type {
      font-weight: 300;
      display: inline-flex;
      align-items: center;
      height: 100%;
    }

    .paper-link {
      color: black;
      text-decoration: none;
      margin-right: 5px;
      font-size: 0.9rem;
    }
    
    .paper-link:hover {
      color: #509A23;
      text-decoration: underline;
      cursor: pointer;
    }

    .paper-honor {
      font-weight: 600;
      color: #f9a825; 
    }
  </style>