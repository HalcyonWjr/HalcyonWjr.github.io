<script>
    import SectionTitle from './SectionTitle.svelte';
    export let bioElement;
</script>
  
<section id="bio" bind:this={bioElement}>
    <SectionTitle title="About" />
      
    <p>Hi, I’m Jinrui Wang (王金睿). </p>
    <p>
        I’m entering my thrid year of PhD studies supervised by <a class="med-link" href="http://www.utahinrichs.de/" target="_blank">Dr. Uta Hinrichs</a> and <a class="med-link" href="https://vishub.net/bach" target="_blank">Dr. Benjamin Bach</a> at <a class="med-link" href="https://vishub.net" target="_blank">Visual+Interactive Lab</a>, The University of Edinburgh. My research focuses on visualization atlases as an emerging form of open data visualizations and effective design of public data representation. I'm passionate about practical project in data exploration and interactive visualization design.
    </p>

    <p class="prior">Prior to this...</p>

    <p class="bullet-point"> Visualization developer (RA) with <a href="https://peacerep.org" target="_blank" class="med-link">PeaceRep</a>, Edinburgh Law School</p>
    <p class="bullet-point"> 🎓 MSc Design Informatics (with distinction), The University of Edinburgh</p>

</section>


<style>
.prior {
    margin: 0;
    margin-top: 20px;
    margin-bottom: 10px;
    font-weight: 500;
}

.med-link {
    font-weight: 600;
    color: #333;
    text-decoration: underline;
    text-decoration-style:wavy;
}
</style>

