<script>
	import image1 from '../../images/9.jpg';
	import image2 from '../../images/11.jpg';
	import image3 from '../../images/15.jpg';
	import FaArrowAltCircleRight from 'svelte-icons/fa/FaArrowAltCircleRight.svelte';
	import FaArrowAltCircleLeft from 'svelte-icons/fa/FaArrowAltCircleLeft.svelte';
	let slideID = 0;
	const images = [image1, image2, image3];

	let touchStartX = 0;
	let touchEndX = 0;

	let mouseDownX = 0;
	let mouseMoveX = 0;
	let isDragging = false;

	function slideLeft() {
		if (slideID > 0) {
			slideID--;
		} else {
			slideID = images.length - 1;
		}
	}
	function slideRight() {
		if (slideID < images.length - 1) {
			slideID++;
		} else {
			slideID = 0;
		}
	}

	function handleTouchStart(event) {
		touchStartX = event.touches[0].clientX;
	}

	function handleTouchMove(event) {
		touchEndX = event.touches[0].clientX;
	}

	function handleTouchEnd() {
		if (touchStartX - touchEndX > 50) {
			slideRight();
		} else if (touchEndX - touchStartX > 50) {
			slideLeft();
		}
	}

	function handleMouseDown(event) {
		isDragging = true;
		mouseDownX = event.clientX;
	}

	function handleMouseMove(event) {
		if (isDragging) {
			mouseMoveX = event.clientX;
		}
	}

	function handleMouseUp() {
		if (isDragging) {
			isDragging = false;
			if (mouseDownX - mouseMoveX > 50) {
				slideRight();
			} else if (mouseMoveX - mouseDownX > 50) {
				slideLeft();
			}
		}
	}

	function handleMouseLeave() {
		if (isDragging) {
			isDragging = false;
		}
	}
</script>

<!-- svelte-ignore a11y-no-static-element-interactions -->
<section
	class="image-slider"
	style="background-image: url({images[slideID]})"
	on:touchstart={handleTouchStart}
	on:touchmove={handleTouchMove}
	on:touchend={handleTouchEnd}
	on:mousedown={handleMouseDown}
	on:mousemove={handleMouseMove}
	on:mouseup={handleMouseUp}
	on:mouseleave={handleMouseLeave}
>
	<button class="arrow-left" on:click={slideLeft}>
		<FaArrowAltCircleLeft></FaArrowAltCircleLeft>
	</button>
	<button class="arrow-right" on:click={slideRight}>
		<FaArrowAltCircleRight></FaArrowAltCircleRight>
	</button>
</section>

<style>
	.image-slider {
		height: 700px;
		position: relative;
		background-repeat: no-repeat;
		background-position: center;
		background-size: cover;
		transition: 0.3s;
	}
	.image-slider * {
		box-sizing: border-box;
	}
	.arrow-left,
	.arrow-right {
		border: none;
		background: #fff;
		position: absolute;
		top: 40%;
		width: 3em;
		height: 3em;
		border-radius: 50%;
		display: flex;
		justify-content: center;
		align-items: center;
		cursor: pointer;
		transition: 0.3s;
	}
	.arrow-left:hover,
	.arrow-right:hover {
		background: #000;
		color: #fff;
	}

	.arrow-left {
		left: 1em;
	}
	.arrow-right {
		right: 1em;
	}
</style>
