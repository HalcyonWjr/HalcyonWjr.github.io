<script>
    import SectionTitle from './SectionTitle.svelte';
    let isCollapsed = true;
</script>
  
<section id="news">
    <SectionTitle title="News" />
    
    {#each newsItems as item, index}
        {#if isCollapsed ? index < 5 : true}
            <p class="news-item">{@html item}</p>
        {/if}
    {/each}
    
    {#if newsItems.length > 5}
        <button on:click={() => isCollapsed = !isCollapsed}>
            {isCollapsed ? '↓ Show More ↓' : '↑ Show Less ↑'}
        </button>
    {/if}
</section>

<script context="module">
    export const newsItems = [
        'Oct 25 :: I am one of the student volunteers for <span class="venue-text">IEEE VIS 2025</span>. See you all in Vienna!',
        'Sept 25 :: Is the third year starting already?! Time flies🏃‍♀️!',
        'Aug 25 :: Our paper on <a href="https://hal.science/view/index/docid/5199752" target="_blank">Visualization Badges</a> is accepted by <span class="venue-text">IEEE VIS 2025</span> with Honorable Mention 🎉!',
        'Aug 25 :: Wow we have two VIS posters! Check these out 👉 <a href="/vis25-poster-atlas.pdf">The Co-Benefits Atlas</a> and <a href="/vis25-poster-peacerep.pdf">Visualizing Peace Transitions</a>',
        'May 25 :: We launched the beta version of <a href="https://ukcobenefitsatlas.net/" target="_blank">The UK Co-Benefits Atlas</a> at ECCI! Amazing work team!',
        'Oct 24 :: I will be one of the student volunteers for <span class="venue-text">IEEE VIS 2024</span>, see you all virtually!',
        'Aug 24 :: Our pictorial and exhibition piece "Pieces of Peace: Women and Gender in Peace Agreements" is accepted by <span class="venue-text">IEEE VIS Art Program</span> 🎨.',
        'July 24 :: Our paper "Visualization Atlases: Explaining and Exploring Complex Topics Through Data, Visualization, and Narration" is accepted by <span class="venue-text">IEEE VIS 2024</span> 🎉.',
        'Nov 23 :: Volunteer at <a class="venue-text" href="https://informationplusconference.com/2023/" target="_blank">Information+ Conference</a> in Edinburgh.',
        'Sep 23 :: I joined Visual+Interactive Lab as a PhD student.',
        'Aug 23 :: Our short paper “Show Me My Users: A Dashboard Visualizing User Interaction Logs” got accepted by <a href="https://ieeevis.org/year/2023/info/papers-sessions" target="_blank">VIS 2023</a> 🎉.',
        'May 23 :: Sarah Shottler and I won <a href="https://www.cdcs.ed.ac.uk/cdcs-prizes" target="_blank">CDCS Digital Research Prize for Best Data Visualisation</a> 🏆 for visualising Russian-Ukraine conflict with PeaceRep!'
    ];
</script>
