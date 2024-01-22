<script>
    import SectionTitle from './SectionTitle.svelte';
  </script>
  
  <section id="publications">
    <SectionTitle title="Publication" />

    <div>
      <p class="paper-title">Show Me My Users: A Dashboard Visualizing User Interaction Logs</p>
      <p><span class="author-emphasis">Jinrui Wang</span>, Mashael AlKadi, Benjamin Bach</p>
      <div class="source">
        <p><span class="conference-name">VIS 23'</span><span class="paper-type"> (short paper)</span> IEEE Visualization and Visual Analytics (VIS), Melbourne, Australia,  2023</p>
      </div>
      <div>
        <a class="paper-link" href="https://www.computer.org/csdl/proceedings-article/vis/2023/255700a156/1T3cP4m2E3m" target="_blank">[ paper ]</a>
        <a class="paper-link" href="https://github.com/HalcyonWjr/Vistorian_Dashboard" target="_blank">[ github ]</a>
        <a class="paper-link" href="https://halcyonwjr.github.io/Vistorian_Dashboard/" target="_blank">[ live demo ]</a>
      </div>
    </div>

  </section>
  
  <style>
    .source {
      display: flex;
      flex-wrap: wrap; 
      gap: 10px; 
      text-align: center;
      align-items: center;
    }

    .source p {
      margin: 0; 
      white-space: nowrap; 
    }

    .paper-title{
      font-weight: 500;
      font-size: 1.05rem;
      margin-bottom: 8px;
    }

    .conference-name {
      border: 1px solid #509A23; 
      border-radius: 5px; 
      padding: 1px;
      margin-right: 5px;
    }

    .author-emphasis {
      font-weight: 500;
    }

    .paper-type {
      font-weight: 300;
    }

    .paper-link {
      color: black;
      text-decoration: none;
      margin-right: 5px;
    }
    
    .paper-link:hover {
      color: #509A23;
      text-decoration: underline;
    }
  </style>