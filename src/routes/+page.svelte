<script>
    import '../app.css';
    import Socials from "../components/Others/Socials.svelte";
    import Navbar from "../components/Navbars/Navbar.svelte";
    import FLipCard from "../components/Cards/FlipCard.svelte"
	import Navbar2 from '../components/Navbars/Navbar2.svelte';
    
</script>

<section>
<Navbar></Navbar>
</section>
<section>
<Navbar2></Navbar2>
</section>
<section>
<FLipCard 
routeTo="/" 
title="Iceland" 
imageSource="https://images.unsplash.com/photo-1476610182048-b716b8518aae?q=80&w=1000&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8NHx8aWNlbGFuZHxlbnwwfHwwfHx8MA%3D%3D">
Iceland has the worlds most beautiful views
</FLipCard>
</section>
<section>
<Socials></Socials>
</section>


<style lang="postcss">
	:global(html) {
		background-color: theme(colors.indigo.400);
	}
</style>
