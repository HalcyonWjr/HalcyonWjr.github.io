<script>
    import Sidebar from './Sidebar.svelte';
    import Bio from './Bio.svelte';
    import News from './News.svelte';
    import Publications from './Publications.svelte';
    import Projects from './Projects.svelte';
    import Footer from './Footer.svelte';

  </script>

<svelte:head>
    <title>Jinrui Wang</title> 
</svelte:head>


  <div class="container">
    <Sidebar />
    <div class="main-content">
      <Bio />
      <News />
      <Publications />
      <Projects />
    </div>
  </div>

  <Footer />
