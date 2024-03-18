<script>
	import { goto } from '$app/navigation';
	export let imageSource;
	export let title;
	export let routeTo = '/';
</script>

<div class="card" style={`background-image: url(${imageSource})`}>
	<div class="info">
		<div class="flex flex-col justify-start items-start">
			<h1 class="text-lg">{title}</h1>
			<p><slot /></p>
		</div>
		<a href={routeTo}>Show Me</a>
	</div>
</div>

<style>
	* {
		box-sizing: border-box;
	}

	body,
	html {
		width: 100%;
		height: 100%;
		display: flex;
		align-items: center;
		justify-content: center;
		background: orange;
	}

	.card {
		width: 320px;
		height: 180px;
		margin: 20px 10px;
		border-radius: 15px;
		padding: 1.5rem;
		background: white;
		position: relative;
		display: flex;
		align-items: flex-end;
		transition: 0.4s ease-out;
		box-shadow: 0px 7px 10px rgba(0, 0, 0, 0.5);

		background-size: 100% 100%;
		background-repeat: no-repeat;
		background-position: center;
	}
	.card:hover {
		transform: translateY(20px);
	}
	.card:hover:before {
		opacity: 1;
	}
	.card:hover .info {
		opacity: 1;
		transform: translateY(0px);
	}
	.card:before {
		content: '';
		position: absolute;
		top: 0;
		left: 0;
		display: block;
		width: 100%;
		height: 100%;
		border-radius: 15px;
		background: rgba(0, 0, 0, 0.6);
		backdrop-filter: blur(5px);
		z-index: 2;
		transition: 0.5s;
		opacity: 0;
	}

	.card .info {
		position: relative;
		display: flex;
		flex-direction: column;
		align-items: start;
		justify-content: space-between;
		z-index: 3;
		color: white;
		opacity: 0;
		transform: translateY(30px);
		transition: 0.5s;
	}
	.card .info h1 {
		margin: 0px;
	}
	.card .info p {
		letter-spacing: 1px;
		font-size: 15px;
		margin-top: 8px;
	}
	.card .info a {
		padding: 0.6rem;
		outline: none;
		border: none;
		border-radius: 3px;
		background: white;
		color: black;
		font-weight: bold;
		cursor: pointer;
		transition: 0.4s ease;
		margin-top: 5px;
	}
	.card .info a:hover {
		background: dodgerblue;
		color: white;
	}

	@media (min-width: 480px) {
		.card {
			width: 360px;
			height: 220px;
			margin: 20px 10px;
		}
	}
	@media (min-width: 850px) {
		.card {
			width: 300px;
			height: 200px;
			margin: 20px 10px;
		}
	}
	@media (min-width: 1300px) {
		.card {
			width: 400px;
			height: 260px;
			margin: 20px 10px;
		}
	}
</style>
