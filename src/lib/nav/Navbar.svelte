<script>
	import Cookies from '$lib/modals/Cookies.svelte';
	import Login from '$lib/modals/Login.svelte';
	let show_cookies = true;
	let show_login = false;
</script>

{#if show_cookies}
	<Cookies on:close={() => show_cookies = false}/>
{/if}

{#if show_login}
	<Login on:close={() => show_login = false} />
{/if}

<!--navbar starting here-->

<nav class="navbar navbar-expand-lg">
	<div class="container-fluid">
		<a class="navbar-brand" href="#">
			<div class="container osf-logo">
				<img src="static/img/logo/logoosf.png" alt="logo" />
				<div class="text-sm-center">
					<h4 class="osf">OSF</h4>
					<h4 class="academy">Academy</h4>
				</div>
			</div></a
		>
		<button
			class="navbar-toggler"
			type="button"
			data-bs-toggle="collapse"
			data-bs-target="#main_nav"
		>
			<span class="navbar-toggler-icon" />
		</button>
		<div class="collapse navbar-collapse" id="main_nav">
			<ul class="navbar-nav">
				<li class="nav-item dropdown has-megamenu">
					<a class="nav-link dropdown-toggle " href="#" data-bs-toggle="dropdown"> Services </a>
					<div class="dropdown-menu megamenu" role="menu">
						<div class="container menu">
							<div class="wrapper row  ">
								<div class="product column col-3 first">
									<h3>Product categories</h3>
									<ul>
										<li><a href="/404">Accessories </a></li>
										<li><a href="/404">Alcohol </a></li>
										<li><a href="/404">Art </a></li>
										<li><a href="/404">Books </a></li>
										<li><a href="/404">Drink </a></li>
										<li><a href="/404">Electronics </a></li>
										<li><a href="/404">Flowers &amp; Plants </a></li>
										<li><a href="/404">Food </a></li>
									</ul>
								</div>
								<div class="product column col-2 second">
									<ul>
										<li><a href="/404">Gadgets </a></li>
										<li><a href="/404">Garden </a></li>
										<li><a href="/404">Grocery </a></li>
										<li><a href="/404">Home </a></li>
										<li><a href="/404">Jewelry </a></li>
										<li><a href="/404">Kids &amp; Baby </a></li>
										<li><a href="/404">Men's Fashion </a></li>
										<li><a href="/404">Mobile </a></li>
									</ul>
								</div>
								<div class="product column col-2 third">
									<ul>
										<li><a href="/404">Motorcycles </a></li>
										<li><a href="/404">Movies </a></li>
										<li><a href="/404">Music </a></li>
										<li><a href="/404">Office </a></li>
										<li><a href="/404">Pets </a></li>
										<li><a href="/404">Romantic</a></li>
										<li><a href="/404">Sport</a></li>
										<li><a href="/404">Toys </a></li>
									</ul>
								</div>
								<div class="sale column col-2 fourth">
									<h3>Sale</h3>
									<ul>
										<li><a href="/404">Accessories </a></li>
										<li><a href="/404">Alcohol </a></li>
										<li><a href="/404">Art </a></li>
										<li><a href="/404">Books </a></li>
										<li><a href="/404">Drink </a></li>
										<li><a href="/404">Electronics </a></li>
										<li><a href="/404">Flowers &amp; Plants </a></li>
										<li><a href="/404">Food </a></li>
									</ul>
								</div>
								<div class="product column col-3 fifth">
									<ul>
										<img src="static/img/popularitems/menu.jpg" alt="menu" />
									</ul>
								</div>
							</div>
						</div>

						<!-- dropdown-mega-menu.// -->
					</div>
				</li>
				<li class="nav-item "><a class="nav-link" href="#">Company </a></li>
				<li class="nav-item"><a class="nav-link" href="#"> Library </a></li>
				<li class="nav-item"><a class="nav-link" href="#"> Contact Us</a></li>
				<li class="nav-item dropdown">
					<a class="nav-link  dropdown-toggle" href="#" data-bs-toggle="dropdown"> EN </a>
					<ul class="dropdown-menu dropdown-menu-end">
						<li><a class="dropdown-item" href="#"> RO</a></li>
						<li><a class="dropdown-item" href="#"> FR</a></li>
						<li><a class="dropdown-item" href="#"> RU</a></li>
					</ul>
				</li>
				<li class="nav-item dropdown">
					<a class="nav-link  dropdown-toggle" href="#" data-bs-toggle="dropdown"> $ US </a>
					<ul class="dropdown-menu dropdown-menu-end">
						<li><a class="dropdown-item" href="#"> EUR</a></li>
						<li><a class="dropdown-item" href="#">GBP </a></li>
						<li><a class="dropdown-item" href="#">RON </a></li>
					</ul>
				</li>
			</ul>
			<ul class="navbar-nav ms-auto ">
				<li class="nav-item"><a class="nav-link" href=""><i class="bi bi-search" /></a></li>
				<li class="nav-item">
					<a class="nav-link" on:click={() => (show_login = true)}><i class="bi bi-person" /></a>
				</li>
				<li class="nav-item notification">
					<a class="nav-link" href="#"> <i class="bi bi-heart" /></a>
					<span class="notification-count">1</span>
				</li>
				<li class="nav-item notification">
					<a class="nav-link" href="#"><i class="bi bi-bag" /></a>
					<span class="notification-count">2</span>
				</li>
			</ul>
		</div>
		<!-- navbar-collapse.// -->
	</div>
	<!-- container-fluid.// -->
</nav>

<style>
	/* ============ desktop view ============ */
	@media all and (min-width: 992px) {
		.navbar .has-megamenu {
			position: static !important;
		}
		.navbar .megamenu {
			left: 0;
			right: 0;
			width: 100%;
			margin-top: 0;
		}
	}
	/* ============ desktop view .end// ============ */

	/* ============ mobile view ============ */
	@media (max-width: 991px) {
		.navbar.fixed-top .navbar-collapse,
		.navbar.sticky-top .navbar-collapse {
			overflow-y: auto;
			max-height: 90vh;
			margin-top: 10px;
		}
	}
	/* ============ mobile view .end// ============ */

	.navbar {
		height: 90px;
		padding: 0;
		background-color: #fff;
	}

	.nav-item > a {
		height: 80px;
	}

	/* we need :global here so svelte doesn't remove this css rule */
	.nav-item > :global(a.show) {
		color: #ffffff;
		background-color: #262a32;
	}

	.navbar .megamenu {
		padding: 0px;
	}
	.navbar-nav{
		margin-left:120px;
		
	}
	.container {
		max-width: 100%;
	}
	.container-fluid {
		padding: 0px 50px;
		margin-top:20px;
	}
	.menu {
		background-color: #262a32;
		display: inline-block;
		width: 100%;
		height: 385px;
	}
	.menu .row {
		padding: 60px 60px;
	}

	.menu a {
		list-style: none;
		text-decoration: none;
		color: #fff;
		font-family: Lato, sans-serif;
		line-height: 2;
		font-size: 16px;
	}
	.first h3 {
		list-style: none;
		text-decoration: none;
		text-transform: uppercase;
		text-align: left;
		color: #fff;
		font-family: Lato, sans-serif;
		font-size: 18px;
	}
	.fourth h3 {
		list-style: none;
		text-decoration: none;
		text-transform: uppercase;
		text-align: left;
		color: #fff;
		font-family: Lato, sans-serif;
		font-size: 18px;
	}
	.first ul {
		padding-left: 0;
	}
	.second {
		padding-top: 30px;
		padding-left: 0px;
		padding-right: 0px;
	}
	.third {
		padding-top: 30px;
		padding-left: 0px;
		padding-right: 0px;
	}
	.fourth {
		padding-left: 0px;
		padding-right: 0px;
	}
	.fourth ul {
		padding: 0;
	}
	.fourth a {
		text-align: left;
	}
	.fifth {
		padding-left: 0px;
		padding-right: 0px;
	}
	.fifth img {
		width: 270px;
		height: 275px;
	}
	.fifth ul {
		padding-left: 0px;
	}
	a {
		color: black;
	}
	.nav-item {
		padding: 0px 10px;
	}
	.bi-person {
		cursor: pointer;
	}
	h4 {
		text-align: center;
	}
	.osf-logo {
		width: 200px;

		
	}

	.osf-logo img {
		float: left;
		
	}
	.osf-logo .osf {
		color: #011847;
		font-weight: 900;
		letter-spacing: 0.28rem;
		margin-bottom: 0px;
		text-decoration-style: solid;
		line-height: 0.8em;
		font-size: 41px;
	}
	.osf-logo .academy {
		color: #84bc22;
		font-weight: 400;
		font-size: 18px;
		letter-spacing: 0.1rem;
		line-height: 1.5em;
	}

	.nav-item {
		font: size 19px;
	}
	.notification {
		position: relative;
	}
	.notification-count {
		color: #84bc22;
		position: absolute;
		top: 0px;
		right: -2px;
		border: 1px solid #84bc22;
		border-radius: 50%;
		padding: 2px 5px;
		font-size: 0.5rem;
		background-color: #fff;
	}
</style>
