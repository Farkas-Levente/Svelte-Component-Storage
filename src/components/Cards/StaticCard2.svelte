<script>
	import DiAngularSimple from 'svelte-icons/di/DiAngularSimple.svelte';
</script>

<div class="card text-white">
	<div class="card-icon text-black">
		<DiAngularSimple></DiAngularSimple>
	</div>
	<h3 class="card-title">Web Development</h3>
	<p class="description">
		Lorem ipsum dolor sit amet conse ctetur adipisicing elit. Qui quaerat fugit quas veniam
		perferendis repudiandae sequi, dolore quisquam illum.
	</p>
</div>

<style>
	.card {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		text-align: center;
		max-width: 300px;
		padding: 20px;
		border-radius: 40px;
		background: linear-gradient(rgb(54, 184, 227), rgb(39, 30, 90));
	}
	.card-icon {
		font-size: 50px;
		line-height: 80px;
		width: 80px;
		height: 80px;
		margin: 0 auto 20px;
		border-radius: 20px;
		box-shadow: 0 0 5px rgba(0, 0, 0, 0.2);
	}

	.card-title {
		width: 300px;
		padding: 10px 0;
		color: #36b8e3;
		background-color: #fff;
		font-size: 18px;
		font-weight: 600;
		text-transform: uppercase;
	}
</style>
