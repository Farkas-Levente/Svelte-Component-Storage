<header>
	<div class="logo">Levi</div>
	<input type="checkbox" id="nav_check" hidden />
	<nav>
		<ul>
			<li>
				<a href="/" class="active">Home</a>
			</li>
			<li>
				<a href="/">Portfolio</a>
			</li>
			<li>
				<a href="/">Blog</a>
			</li>
			<li>
				<a href="/">Services</a>
			</li>
			<li>
				<a href="/">About</a>
			</li>
		</ul>
	</nav>
	<label for="nav_check" class="hamburger">
		<div></div>
		<div></div>
		<div></div>
	</label>
</header>

<style>
	header {
		background: #fff;
		width: 100%;
		height: 70px;
		display: flex;
		align-items: center;
		justify-content: space-between;
		padding: 0 50px;
	}
	header .logo {
		font-size: 30px;
		text-transform: uppercase;
	}
	header nav ul {
		display: flex;
	}
	header nav ul li a {
		display: inline-block;
		color: #000;
		padding: 5px 0;
		margin: 0 10px;
		border: 3px solid transparent;
		text-transform: uppercase;
		transition: 0.2s;
	}
	header nav ul li a:hover,
	header nav ul li a.active {
		border-bottom-color: dodgerblue;
	}
	.hamburger {
		cursor: pointer;
		display: none;
	}
	.hamburger div {
		width: 30px;
		height: 3px;
		margin: 5px 0;
		background: #000;
	}
	@media only screen and (max-width: 900px) {
		header {
			padding: 0 30px;
		}
	}
	@media only screen and (max-width: 700px) {
		.hamburger {
			display: block;
		}
		header nav {
			z-index: 100;
			position: absolute;
			width: 70%;
			height: 100%;
			left: -100%;
			top: 70px;

			background: #fff;
			padding: 30px;
			transition: 0.3s;
		}
		header #nav_check:checked ~ nav {
			left: 0;
		}
		header nav ul {
			display: block;
		}
		header nav ul li a {
			margin: 5px 0;
		}
	}
</style>
