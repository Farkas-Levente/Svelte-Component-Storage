<script>
	import FaGithubSquare from 'svelte-icons/fa/FaGithubSquare.svelte';
	import FaTwitterSquare from 'svelte-icons/fa/FaTwitterSquare.svelte';
	import FaYoutubeSquare from 'svelte-icons/fa/FaYoutubeSquare.svelte';
	
</script>

<div
	id="contact"
	class="
sm:gap-5 sm:h-28 sm:flex-row

gap-3 h-40 flex-col pl-4 pr-4 text-center
flex items-center justify-center w-full text-white bg-black "
>
	<div class=" flex items-center justify-center w-12 h-12">
		<img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRGKGuCeQ4gs9_R3qjCT_v4TQ1wdbeLq3b9JA&usqp=CAU" class="rounded-full" alt="Logo" />
	</div>
	<div class="text-xl font-semibold">
		Have a look at our <span class="text-primary">Social Media:</span>
	</div>
	<div class="flex flex-row gap-2 justify-center">
		<div class=" flex justify-center items-center orange-hover">
			<a
				href="https://www.youtube.com/channel/UCGkrvPlFmQ6bqaq4HG2XAqw"
				target="_blank"
				class="w-10 h-10 hover:text-orange-400"
			>
				<FaYoutubeSquare></FaYoutubeSquare></a
			>
		</div>
		<div class=" flex justify-center items-center orange-hover">
			<a href="https://github.com/wolfdencode/" target="_blank" class="w-10 h-10 hover:text-orange-400" >
				<FaGithubSquare></FaGithubSquare></a
			>
		</div>
		<div class=" flex justify-center items-center orange-hover">
			<a class="w-10 h-10 hover:text-orange-400" href="https://twitter.com/WolfDenCode" target="_blank">
				<FaTwitterSquare></FaTwitterSquare></a
			>
		</div>
	</div>
</div>
