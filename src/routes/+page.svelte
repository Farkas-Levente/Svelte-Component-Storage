<script>
	import '../app.css';
	import Socials from '../components/Others/Socials.svelte';
	import Navbar from '../components/Navbars/Navbar.svelte';
	import FLipCard from '../components/Cards/FlipCard.svelte';
	import Navbar2 from '../components/Navbars/Navbar2.svelte';
	import FLipCard2 from '../components/Cards/FLipCard2.svelte';
</script>

<section>
	<Navbar></Navbar>
</section>
<section>
	<Navbar2></Navbar2>
</section>
<section class="middle">
	<FLipCard
		routeTo="/"
		title="Iceland"
		imageSource="https://images.unsplash.com/photo-1476610182048-b716b8518aae?q=80&w=1000&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8NHx8aWNlbGFuZHxlbnwwfHwwfHx8MA%3D%3D"
	>
		Iceland has the worlds most beautiful views
	</FLipCard>
	<FLipCard
		routeTo="/"
		title="Iceland"
		imageSource="https://images.unsplash.com/photo-1476610182048-b716b8518aae?q=80&w=1000&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8NHx8aWNlbGFuZHxlbnwwfHwwfHx8MA%3D%3D"
	>
		Iceland has the worlds most beautiful views
	</FLipCard>
	<FLipCard
		routeTo="/"
		title="Iceland"
		imageSource="https://images.unsplash.com/photo-1476610182048-b716b8518aae?q=80&w=1000&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8NHx8aWNlbGFuZHxlbnwwfHwwfHx8MA%3D%3D"
	>
		Iceland has the worlds most beautiful views
	</FLipCard>
</section>
<section class="middle">
	<FLipCard2 imageSrc="https://picsum.photos/id/287/250/300">The Day</FLipCard2>
	<FLipCard2 imageSrc="https://picsum.photos/id/287/250/300">The Day</FLipCard2>
	<FLipCard2 imageSrc="https://picsum.photos/id/287/250/300">The Day</FLipCard2>
</section>
<section>
	<Socials></Socials>
</section>

<style lang="postcss">
	:global(html) {
		background-color: theme(colors.indigo.400);
	}

	.middle {
		display: flex;
		justify-content: center;
		text-align: center;
		flex-wrap: wrap;
	}
</style>
