<script>
    import SectionTitle from './SectionTitle.svelte';
    export let bioElement;
</script>
  
<section id="bio" bind:this={bioElement}>
    <SectionTitle title="About" />
      
    <p>Hi, I’m Jinrui Wang (王金睿). </p>
    <p>
        I’m a third year PhD student supervised by <a class="med-link" href="http://www.utahinrichs.de/" target="_blank">Dr. Uta Hinrichs</a> and <a class="med-link" href="https://vishub.net/bach" target="_blank">Dr. Benjamin Bach</a> at <a class="med-link" href="https://vishub.net" target="_blank">Visual+Interactive Lab</a>, The University of Edinburgh. Before that, I completed my MSc in Design Informatics (with distinction) at the University of Edinburgh (2022) and BEcon at University of International Business and Economics in Beijing (2020). My PhD research focuses on visualization atlases as an emerging form of visualization for communicating complex datasets to wide range of audiences. I'm passionate about research through practical designs in interactive data exploration.
    </p>

    <p class="prior">My ongoing projects👩🏻‍💻:</p>

    <p class="bullet-point"> Designing a visualization atlas on the social co-benefits of climate mitigation datasets with <a href="https://edinburghcentre.org" target="_blank" class="med-link">Edinburgh Climate Change Insitute</a>.</p>
    <p class="bullet-point"> Visualizing peace transistion data with <a href="https://peacerep.org" target="_blank" class="med-link">PeaceRep</a>, Edinburgh Law School.</p>

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

