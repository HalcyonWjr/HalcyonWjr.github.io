<script>
    import SectionTitle from './SectionTitle.svelte'
    import ProjectCard from './ProjectCard.svelte';
  </script>
  
  <section id="projects">
    <SectionTitle title="Projects" />

    <ProjectCard 
      title="Pieces of Peace: Women and Gender in Peace Agreements" 
      date="Jun 2024 - VIS Art Program"
      description="Physicalization of women and gender issues mentioned in the Afghanistan post 2000s intervention process using debossing technique."
      imageUrl="/peace.png"
      projectUrl="https://www.designinformatics.org/news/pieces-of-peace-reflection/"
    />

    <ProjectCard 
      title="Responsible AI Community Network" 
      date="Aug 2023, with Braid"
      description="Large screen network display for visualizing interdisciplinary community at the launch of BRAID: Bridging Responsible AI Divides programme."
      imageUrl="/braidvis.png"
      projectUrl="https://braidvis.onrender.com"
    />

    <ProjectCard 
    title="VisActivity Platform" 
    date="Apr 2022 - Jun 2023, with DDI small grant"
    description="Designed and developed the front-end for a platform collecting data physicalization activities."
    imageUrl="/visactivities.png"
    />

    <ProjectCard 
    title="Russia as a Global Peace Actor" 
    date="Nov 2022 - Mar 2023, with PeaceRep"
    description="Actor network dashboard visualizing Russia's involvement in peace and transition processes, in collaboration with PeaceRep project."
    imageUrl="/actor-network.png"
    projectUrl="https://actor-network-russia.onrender.com"
    />

    <ProjectCard 
    title="Vistorian Dashboard" 
    date="Apr - Aug 2023, MSc Project"
    description="A three-page interactive dashboard display depicting overall user activity, visualization diagram comparison and individual session timeline."
    imageUrl="/vistorian-dashboard.png"
    projectUrl="https://github.com/HalcyonWjr/Vistorian_Dashboard"
    />

  </section>
  