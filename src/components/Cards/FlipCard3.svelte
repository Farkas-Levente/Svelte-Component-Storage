<script>
	import FaLongArrowAltRight from 'svelte-icons/fa/FaLongArrowAltRight.svelte';
	export let imageSrc;
	export let title;
	export let titleOffsetPX = 300;
</script>

<div class="card" style="--offset:{titleOffsetPX + 'px'}">
	<img src={imageSrc} alt="" />

	<div class="card-content">
		<h2>{title}</h2>
		<p>
			<slot />
		</p>
		<a href="/" class="button flex flex-row items-center justify-center gap-2">
			Find out more
			<span class="material-symbols-outlined">
				<div class="w-5 h-5">
					<FaLongArrowAltRight></FaLongArrowAltRight>
				</div>
			</span>
		</a>
	</div>
</div>

<style>
	.card {
		width: 300px;
		height: 450px;
		border-radius: 10px;
		overflow: hidden;
		cursor: pointer;
		position: relative;
		color: white;
		box-shadow: 0 10px 30px 5px rgba(0, 0, 0, 0.2);
		margin: 20px 0;
		background-color: #000000;
	}
	img {
		position: absolute;
		object-fit: cover;
		width: 100%;
		height: 100%;
		top: 0;
		left: 0;
		opacity: 0.8;
		transition: opacity 0.2s ease-out;
	}

	h2 {
		position: absolute;
		inset: auto auto 30px 30px;
		margin: 10px 0;
		font-size: x-large;
		transition: inset 0.3s 0.3s ease-out;
		font-family: 'Roboto Condensed', sans-serif;
		font-weight: normal;
		text-transform: uppercase;
	}

	p,
	a {
		position: absolute;
		opacity: 0;
		max-width: 80%;
		transition: opacity 0.3s ease-out;
	}

	p {
		text-align: left;
		inset: auto auto 80px 30px;
	}

	a {
		inset: auto auto 40px 30px;
		color: inherit;
		text-decoration: none;
	}

	.card:hover h2 {
		inset: auto auto var(--offset) 30px;
		transition: inset 0.3s ease-out;
	}

	.card:hover p,
	.card:hover a {
		opacity: 1;
		transition: opacity 0.5s 0.1s ease-in;
	}

	.card:hover img {
		transition: opacity 0.3s ease-in;
		opacity: 0.3;
	}

	.material-symbols-outlined {
		vertical-align: middle;
	}
</style>
