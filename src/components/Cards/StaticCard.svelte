<script>
	export let subtext;
	export let color;
</script>

<div class="ag-courses_item" style="--theme-color: {color}">
	<a href="/" class="ag-courses-item_link">
		<div class="ag-courses-item_bg"></div>

		<div class="ag-courses-item_title">
			<slot />
		</div>

		<div class="ag-courses-item_date-box">
			{subtext}
		</div>
	</a>
</div>

<style>
	.ag-courses_item {
		-ms-flex-preferred-size: calc(33.33333% - 30px);

		margin: 0 15px 30px;

		overflow: hidden;

		border-radius: 28px;
	}
	.ag-courses-item_link {
		width: 300px;
		display: block;
		padding: 30px 20px;
		background-color: #121212;

		overflow: hidden;

		position: relative;
	}
	.ag-courses-item_link:hover,
	.ag-courses-item_link:hover .ag-courses-item_date {
		text-decoration: none;
		color: #fff;
	}
	.ag-courses-item_link:hover .ag-courses-item_bg {
		-webkit-transform: scale(12);
		-ms-transform: scale(12);
		transform: scale(12);
	}
	.ag-courses-item_title {
		min-height: 87px;
		margin: 0 0 25px;

		overflow: hidden;

		font-weight: bold;
		font-size: 30px;
		color: #fff;

		z-index: 2;
		position: relative;
	}
	.ag-courses-item_date-box {
		font-size: 18px;
		color: #fff;

		z-index: 2;
		position: relative;
	}
	.ag-courses-item_date {
		font-weight: bold;
		color: var(--theme-color);

		-webkit-transition: color 0.5s ease;
		-o-transition: color 0.5s ease;
		transition: color 0.5s ease;
	}
	.ag-courses-item_bg {
		height: 128px;
		width: 128px;
		background-color: var(--theme-color);

		z-index: 1;
		position: absolute;
		top: -75px;
		right: -75px;

		border-radius: 50%;

		-webkit-transition: all 0.5s ease;
		-o-transition: all 0.5s ease;
		transition: all 0.5s ease;
	}

	@media only screen and (max-width: 979px) {
		.ag-courses_item {
			-ms-flex-preferred-size: calc(50% - 30px);
		}
		.ag-courses-item_title {
			font-size: 24px;
		}
	}

	@media only screen and (max-width: 639px) {
		.ag-courses_item {
			-ms-flex-preferred-size: 100%;
			text-align: center;
			display: flex;
			justify-content: center;
			text-align: center;
		}
		.ag-courses-item_title {
			min-height: 72px;
			line-height: 1;

			font-size: 24px;
		}
		.ag-courses-item_link {
			padding: 22px 40px;
		}
		.ag-courses-item_date-box {
			font-size: 16px;
		}
	}
</style>
