<script>
	import '../app.css';
	import Socials from '../components/Others/Socials.svelte';
	import Navbar from '../components/Navbars/Navbar.svelte';
	import FLipCard from '../components/Cards/FlipCard.svelte';
	import Navbar2 from '../components/Navbars/Navbar2.svelte';
	import FLipCard2 from '../components/Cards/FLipCard2.svelte';
	import StaticCard from '../components/Cards/StaticCard.svelte';
	import FlipCard3 from '../components/Cards/FlipCard3.svelte';
	import StaticCard2 from '../components/Cards/StaticCard2.svelte';
	import GoogleMap from '../components/Others/GoogleMap.svelte';
	import Slider from '../components/Others/Slider.svelte';
</script>

<section>
	<Navbar></Navbar>
</section>
<section>
	<Navbar2></Navbar2>
</section>
<section class="middle -z-10">
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
<section class="middle gap-10">
	<FlipCard3
		titleOffsetPX="200"
		imageSrc="https://img.freepik.com/premium-photo/free-photo-beautiful-nature-hd-8k-wallpaper-stock-photographic-image_915071-68230.jpg"
		title="Frozen Lake"
		>This is the filler text that will show you the description of the image or whatever you want to
		see and it will darken the view.</FlipCard3
	>
	<FlipCard3
		titleOffsetPX="200"
		imageSrc="https://img.freepik.com/premium-photo/free-photo-beautiful-nature-hd-8k-wallpaper-stock-photographic-image_915071-68230.jpg"
		title="Frozen Lake"
		>This is the filler text that will show you the description of the image or whatever you want to
		see and it will darken the view.</FlipCard3
	>
	<FlipCard3
		titleOffsetPX="200"
		imageSrc="https://img.freepik.com/premium-photo/free-photo-beautiful-nature-hd-8k-wallpaper-stock-photographic-image_915071-68230.jpg"
		title="Frozen Lake"
		>This is the filler text that will show you the description of the image or whatever you want to
		see and it will darken the view.</FlipCard3
	>
</section>
<section class="middle mt-10">
	<StaticCard color="#3ecd53" subtext="Subtext comes here">Some text to fill the space.</StaticCard>
	<StaticCard color="#e44002" subtext="Subtext comes here">Some text to fill the space.</StaticCard>
	<StaticCard color="#cd3e94" subtext="Subtext comes here">Some text to fill the space.</StaticCard>
</section>

<section class="middle mt-10 mb-10 gap-10">
	<StaticCard2></StaticCard2>
	<StaticCard2></StaticCard2>
	<StaticCard2></StaticCard2>
</section>
<section>
	<GoogleMap></GoogleMap>
</section>
<section class=" mb-56 mt-56">
	<Slider></Slider>
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
