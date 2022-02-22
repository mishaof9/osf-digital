<script>
	import Navbar from '$lib/Navbar.svelte';
	import Footer from '$lib/Footer.svelte';
</script>

<Navbar />

<div class="wrapper home-404">
	<ul>
		<li class="li-home"><a href="index.html">Home</a></li>
		<li class="li-empty">/</li>
		<li class="li-404">404</li>
	</ul>
	<h2>404</h2>
</div>

<div class="main-error">
	<div class="oops">
		<div class="centered">Oops!</div>
	</div>

	<div class="info">
		<h3>Sorry, this page could not be found!</h3>
		<p>
			Aenean commodo ligula eget dolor. Aenean massa. Cum sociis natoque penatibus <br />et magnis
			dis parturient montes, nascetur ridiculus mus.
		</p>
		<p>
			Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula<br />
			eget dolor. Aenean massa.
		</p>
		<a href="index.html">Go back to Homepage</a>
		<h3>Search our site</h3>
		<div class="search">
			<input type="text" placeholder="SEARCH" />
			<i class="bi bi-search" />
		</div>
	</div>
</div>

<Footer />

<style>
	body {
		background-color: #f1edea;
	}
	.main-error {
		background-color: #ffffff;
		margin-left: 50px;
		margin-right: 50px;
		margin-top: 90px;
		height: 450px;
		margin-bottom: 40px;
	}

	.home-404 {
		width: 100%;
		align-self: center;
		margin-top: 100px;
	}
	.home-404 ul {
		display: flex;
		list-style: none;
		justify-content: center;
		left: 545px;
		top: -55px;
	}
	.li-home a {
		text-decoration: none;
		font-family: Lato;
		font-size: 17px;
		color: #84bc22;
		font-weight: bold;
	}
	.li-404 {
		font-family: Lato;
		font-size: 17px;
		color: black;
		font-weight: bold;
	}
	.li-empty {
		padding-left: 10px;
		padding-right: 10px;
	}
	.home-404 h2 {
		text-align: center;
		font-family: Lato;
		font-size: 64px;
		margin-left: 30px;
		padding-top: 20px;
	}
	.oops {
		margin-top: 35px;
		float: left;
		width: 366px;
		height: 366px;
		background: url(static/img/404/oops.png) -100px no-repeat;
	}
	.oops .centered {
		margin-top: 55px;
		margin-left: 30px;
		font-family: Lato;
		font-size: 125px;
		font-weight: bold;
		color: #84bc22;
	}

	.info {
		display: grid;
		padding-left: 75px;
		padding-top: 35px;
	}
	.info h3 {
		font-family: Lato;
		font-size: 26px;
		font-weight: bold;
		padding-bottom: 10px;
	}
	.info p {
		font-family: Lato;
		font-size: 18px;
		padding-top: 0px;
		margin-top: 5px;
	}
	.info a {
		font-family: Lato;
		font-size: 20px;
		color: #84bc22;
		text-decoration: none;
		padding-top: 10px;
		padding-bottom: 10px;
	}
	.info .search {
		position: relative;
		width: 80%;
	}
	.info .search > input {
		border-radius: 35px;
		border: 3px solid #f1edea;
		padding: 5px 10px;
		width: 100%;
		color: #45413e;
		font-size: 12px;
		margin-top: 10px;
	}
	.search i {
		position: absolute;
		right: 15px;
		top: 15px;
		fill: #45413e;
	}
	.info .search > input:focus {
		border-color: #45413e;
	}
</style>
