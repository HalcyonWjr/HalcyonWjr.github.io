<script>
    import SectionTitle from './SectionTitle.svelte';
    let isCollapsed = true;
</script>
  
<section id="news">
    <SectionTitle title="News" />
    
    {#each newsItems as item, index}
        {#if isCollapsed ? index < 5 : true}
            <p class="bullet-point">{@html item}</p>
        {/if}
    {/each}
    
    {#if newsItems.length > 5}
        <button on:click={() => isCollapsed = !isCollapsed}>
            {isCollapsed ? 'Show More' : 'Show Less'}
        </button>
    {/if}
</section>

<script context="module">
    export const newsItems = [
        'Oct 24 :: I will be one of the student volunteers for <a href="https://ieeevis.org/year/2024/welcome">IEEE VIS 2024</a>, see you all virtually!',
        'Aug 24 :: Our pictorial and exhibition piece "Pieces of Peace: Women and Gender in Peace Agreements" is accepted by <a href="https://visap.net/2024/">IEEE VISAP 2024</a>🎨.',
        'July 24 :: Our paper "Visualization Atlases: Explaining and Exploring Complex Topics Through Data, Visualization, and Narration" is accepted by <a href="https://ieeevis.org/year/2024/welcome">IEEE VIS 2024</a>🎉.',
        'Nov 23 :: Volunteer at <a href="https://informationplusconference.com/2023/" target="_blank">Information+ Conference</a> in Edinburgh.',
        'Sep 23 :: I joined Visual+Interactive Lab as a PhD student.',
        'Aug 23 :: Our short paper “Show Me My Users: A Dashboard Visualizing User Interaction Logs” got accepted by <a href="https://ieeevis.org/year/2023/info/papers-sessions" target="_blank">VIS 2023</a> 🎉.',
        'May 23 :: Sarah Shottler and I won <a href="https://www.cdcs.ed.ac.uk/cdcs-prizes" target="_blank">CDCS Digital Research Prize for Best Data Visualisation</a> 🏆 for visualising Russian-Ukraine conflict with PeaceRep!'
    ];
</script>

<style>
    button {
        margin: 5px 0;
    }
</style>
