<script>
	import '../app.css';
	import GoThreeBars from 'svelte-icons/go/GoThreeBars.svelte';
	import GoX from 'svelte-icons/go/GoX.svelte';
	import { writable } from 'svelte/store';
	import icon from '../images/wolficon_cut.png';

	import { onMount } from 'svelte';

	const isOpen = writable(false);

	let componentToScrollTo;

	onMount(() => {
		// Use on:route to detect route changes
		if (componentToScrollTo) {
			componentToScrollTo.scrollIntoView({ behavior: 'smooth' });
		}
	});
</script>

<header class="text-white">
	<div class="navbar">
		<div class=" flex items-center justify-center w-12 h-12">
			<img src={icon} class="rounded-full" alt="Logo" />
		</div>
		<ul class="links">
			<li>
				<a href="/#home"> Home</a>
			</li>

			<li><a href="/projects">Projects</a></li>
			<li>
				<a href="/#contact">Contact</a>
			</li>
		</ul>
		<a href="/#contact" class="action_btn bg-primary">Get Started</a>
		<!-- svelte-ignore a11y-no-static-element-interactions -->
		<div
			on:click={() => {
				$isOpen = !$isOpen;
			}}
			on:keydown={() => {
				$isOpen = !$isOpen;
			}}
			class="toggle_btn"
		>
			{#if !$isOpen}
				<GoThreeBars></GoThreeBars>
			{:else}
				<GoX></GoX>
			{/if}
		</div>
	</div>

	<div class="dropdown_menu {$isOpen ? 'open' : ''}">
		<li>
			<a href="/#home">Home</a>
		</li>
		<li><a href="/projects">Projects</a></li>
		<li>
			<a href="/#contact">Contact</a>
		</li>
		<li><a href="/#contact" class="action_btn bg-primary">Get Started</a></li>
	</div>
</header>

<slot />

<style>
	header {
		position: sticky;
		top: 0;
		bottom: 0;
		background-color: rgba(0, 0, 0, 0.8); /* Adjust the transparency */
		z-index: 1000; /* Ensure the navbar is on top of other elements */
		padding: 0 2rem;
	}
	li {
		list-style: none;
	}
	a {
		text-decoration: none;

		font-size: 1rem;
	}
	a:hover {
		color: orange;
	}

	.navbar {
		width: 100%;
		height: 60px;
		max-width: 1200px;
		margin: 0 auto;
		display: flex;
		align-items: center;
		justify-content: space-between;
	}

	.navbar .links {
		display: flex;
		gap: 2rem;
	}
	.navbar .toggle_btn {
		font-size: 1.5rem;
		cursor: pointer;
		display: none;
		width: 40px;
		height: 40px;
	}
	.action_btn {
		color: white;
		padding: 0.5rem 1rem;
		border: none;
		outline: none;
		border-radius: 20px;
		font-size: 0.8rem;
		font-weight: bold;
		cursor: pointer;
		transition: scale 0.2 ease;
	}
	.action_btn:hover {
		scale: 1.05;
		color: orange;
	}
	.action_btn:active {
		scale: 0.95;
	}

	.dropdown_menu {
		position: absolute;
		right: 2rem;
		top: 100%;
		width: 300px;
		height: 0px;
		background: rgba(255, 255, 255, 0.1);
		backdrop-filter: blur(15px);
		border-radius: 10px;
		overflow: hidden;
		transition: height 0.2s cubic-bezier(0.175, 0.885, 0.32, 1.275);
	}
	.dropdown_menu.open {
		height: 240px;
	}
	.dropdown_menu li {
		padding: 0.7rem;
		display: flex;
		align-items: center;
		justify-content: center;
	}
	.dropdown_menu .action_btn {
		width: 100%;
		display: flex;
		justify-content: center;
	}
	@media (max-width: 992px) {
		.navbar .links,
		.navbar .action_btn {
			display: none;
		}
		.navbar .toggle_btn {
			display: block;
		}
		.navbar .toggle_btn {
			display: block;
		}
		.dropdown_menu {
			display: block;
		}
	}
	@media (max-width: 576px) {
		.dropdown_menu {
			left: 2rem;
			width: unset;
		}
	}
</style>
