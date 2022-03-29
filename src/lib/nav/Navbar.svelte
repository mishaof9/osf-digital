<script>
	import Cookies from '$lib/modals/Cookies.svelte';
	import Login from '$lib/modals/Login.svelte';
	let show_login = false;

	let cart = 0;
	let wishlist = 0;
	function handle_storage() {
		cart = localStorage.getItem('cart');
		wishlist = localStorage.getItem('wishlist');
	}
</script>

<svelte:window
	on:load={handle_storage}
	on:storage={handle_storage}
	on:product_changed={handle_storage}
/>

<Cookies />

{#if show_login}
	<Login on:close={() => (show_login = false)} />
{/if}

<!--navbar starting here-->
<nav class="navbar navbar-expand-lg">
	<button class="navbar-toggler collapsed" data-bs-toggle="collapse" data-bs-target="#navbar">
		<i class="bi bi-list" />
		<i class="bi bi-x-lg" />
	</button>

	<a class="navbar-brand" href="/">
		<img class="osf-logo-small d-lg-none" src="/img/logo/logoosf.png" alt="logo" />

		<div class="osf-logo d-none d-lg-block">
			<div class="row g-1">
				<div class="col">
					<img src="/img/logo/logoosf.png" alt="logo" />
				</div>
				<div class="col">
					<div class="text-center">
						<h4 class="osf">OSF</h4>
						<h4 class="academy">Academy</h4>
					</div>
				</div>
			</div>
		</div>
	</a>

	<div class="navbar-collapse collapse" id="navbar">
		<!-- nav for small screens, with accordion -->
		<div class="navbar-nav d-lg-none accordion accordion-flush" id="menu-acc">
			<li class="nav-item accordion-item">
				<h2 class="accordion-header" id="hdr-services">
					<button
						class="accordion-button collapsed"
						type="button"
						data-bs-toggle="collapse"
						data-bs-target="#coll-services"
						aria-expanded="true"
						aria-controls="coll-services"
					>
						Services
					</button>
				</h2>
				<div
					id="coll-services"
					class="accordion-collapse collapse"
					aria-labelledby="hdr-services"
					data-bs-parent="#menu-acc"
				>
					<ul class="accordion-body list-unstyled">
						<li class="nav-item dropdown">
							<a class="nav-link  dropdown-toggle" href="#" data-bs-toggle="dropdown">
								Product Categories
							</a>
							<ul class="dropdown-menu dropdown-menu-end">
								<li><a href="/404">Accessories </a></li>
								<li><a href="/404">Alcohol </a></li>
								<li><a href="/404">Art </a></li>
								<li><a href="/404">Books </a></li>
								<li><a href="/404">Drink </a></li>
								<li><a href="/404">Electronics </a></li>
								<li><a href="/404">Flowers &amp; Plants </a></li>
								<li><a href="/404">Food </a></li>
								<li><a href="/404">Gadgets </a></li>
								<li><a href="/404">Garden </a></li>
								<li><a href="/404">Grocery </a></li>
								<li><a href="/404">Home </a></li>
								<li><a href="/404">Jewelry </a></li>
								<li><a href="/404">Kids &amp; Baby </a></li>
								<li><a href="/404">Men's Fashion </a></li>
								<li><a href="/404">Mobile </a></li>
								<li><a href="/404">Motorcycles </a></li>
								<li><a href="/404">Movies </a></li>
								<li><a href="/404">Music </a></li>
								<li><a href="/404">Office </a></li>
								<li><a href="/404">Pets </a></li>
								<li><a href="/404">Romantic</a></li>
								<li><a href="/404">Sport</a></li>
								<li><a href="/404">Toys </a></li>
							</ul>
						</li>
						<li class="nav-item dropdown">
							<a class="nav-link  dropdown-toggle" href="#" data-bs-toggle="dropdown">Sale</a>
							<ul class="dropdown-menu dropdown-menu-end">
								<li><a href="/404">Accessories </a></li>
								<li><a href="/404">Alcohol </a></li>
								<li><a href="/404">Art </a></li>
								<li><a href="/404">Books </a></li>
								<li><a href="/404">Drink </a></li>
								<li><a href="/404">Electronics </a></li>
								<li><a href="/404">Flowers &amp; Plants </a></li>
								<li><a href="/404">Food </a></li>
							</ul>
						</li>
					</ul>
				</div>
			</li>
			<li class="nav-itemm"><a class="accordion-button collapsed" href="/404"> Library </a></li>
			<li class="nav-itemm"><a class="accordion-button collapsed" href="/404"> Company </a></li>
			<li class="nav-item accordion-item">
				<h2 class="accordion-header" id="hdr-contact">
					<button
						class="accordion-button collapsed"
						type="button"
						data-bs-toggle="collapse"
						data-bs-target="#coll-contact"
						aria-expanded="true"
						aria-controls="coll-contact"
					>
						Contact
					</button>
				</h2>
				<div
					id="coll-contact"
					class="accordion-collapse collapse"
					aria-labelledby="hdr-contact"
					data-bs-parent="#menu-acc"
				>
					<div class="accordion-body">
						<p>
							Headquarters <br />
							5600, Blvd. des Galeries, Bur 530 <br />
							Quebec,Quebec G2K 2H6.
						</p>
						<p><a href="mailto:contact@osf-global.com">contact@osf-global.com</a></p>
						<p><a href="tel:+1(888)548-4333" id="phone">+1(888)548-4333 </a></p>
					</div>
				</div>
			</li>

			<img src="/img/popularitems/menu.jpg" alt="menu" />
		</div>

		<!-- navs for bigger screens -->
		<div id="menu-nav" class="w-100 d-none d-lg-flex">
			<ul class="navbar-nav mx-auto links">
				<li class="nav-item dropdown has-megamenu">
					<a class="nav-link dropdown-toggle" href="#" data-bs-toggle="dropdown"> Services </a>
					<div class="dropdown-menu megamenu row" role="menu">
						<div class="row h-100">
							<div class="col">
								<h6>Product categories</h6>
								<div class="row">
									<div class="col">
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
									<div class="col">
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
									<div class="col">
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
								</div>
							</div>

							<div class="col col-2">
								<h6>Sale</h6>
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

							<div class="col col-auto">
								<div class="h-100 d-flex justify-content-center">
									<img
										src="/img/popularitems/menu.jpg"
										alt="menu"
										class="img-fluid my-auto"
									/>
								</div>
							</div>
						</div>
					</div>
				</li>
				<li class="nav-item "><a class="nav-link" href="/countdown">Company </a></li>
				<li class="nav-item"><a class="nav-link" href="#"> Library </a></li>
				<li class="nav-item"><a class="nav-link" href="#"> Contact Us</a></li>
			</ul>

			<ul class="navbar-nav prefs">
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

			<ul class="navbar-nav actions">
				<li class="nav-item"><a class="nav-link" href=""><i class="bi bi-search" /></a></li>
				<li class="nav-item">
					<a class="nav-link" on:click={() => (show_login = true)}><i class="bi bi-person" /></a>
				</li>
				<li class="nav-item ">
					<a class="nav-link notification" href="#">
						<i class="bi bi-heart" />
						{#if wishlist > 0}
							<span class="notification-count">{wishlist}</span>
						{/if}
					</a>
				</li>
				<li class="nav-item">
					<a class="nav-link notification" href="#">
						<i class="bi bi-bag" />
						{#if cart > 0}
							<span class="notification-count">{cart}</span>
						{/if}
					</a>
				</li>
			</ul>
		</div>
	</div>
</nav>

<style>
	.navbar {
		justify-content: center;
		background-color: #fff;
		padding: 0;
		border-bottom: 1px solid #f3f0ea;
	}

	#menu-acc {
		background-color: #262a32;
	}

	#menu-acc .accordion-item {
		border: none;
		background-color: inherit;
	}

	#menu-acc .accordion-button {
		background-color: inherit;
		text-transform: uppercase;
		color: #fff;
	}

	#menu-acc .accordion-body {
		background-color: inherit;
		color: #fff;
	}

	#menu-acc .accordion-button:focus {
		border: none;
		box-shadow: none;
	}

	#menu-acc .accordion-button:after {
		font-family: bootstrap-icons !important;
		content: '\F22C';
		color: #fff;
		background: none;
	}

	#menu-acc a.accordion-button:after {
		display: none;
	}

	#menu-acc a {
		text-decoration: none;
		color: #fff;
	}

	#menu-acc img {
		width: 100%;
		padding: 15px;
		border-radius: 20px;
	}

	#menu-acc .dropdown-menu {
		background-color: inherit;
		border: none;
	}

	#menu-nav {
		height: 78px;
	}

	.navbar-toggler {
		position: absolute;
		top: 16px;
		left: 5px;
	}

	.navbar-toggler.collapsed .bi-x-lg {
		display: none;
	}

	.navbar-toggler.collapsed .bi-list {
		display: block;
	}

	.navbar-toggler .bi-list {
		display: none;
	}

	.osf-logo-small {
		height: 42px;
		margin: 10px;
	}

	.osf-logo {
		padding: 0;
		margin-top: 5px;
		margin-left: 56px;
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
		font-weight: 600;
		font-size: 18px;
		letter-spacing: 0.1rem;
		line-height: 1.5em;
	}

	.links .nav-link {
		color: #262a32;
	}

	.navbar .has-megamenu {
		position: static !important;
	}

	.navbar .megamenu {
		left: 0;
		right: 0;
		width: 100%;
		margin-top: 0;
		border: 0;
	}

	/* we need :global here so svelte doesn't remove this css rule */
	#menu-nav :global(a.show) {
		color: #ffffff;
		background-color: #262a32;
		border-bottom: 2px solid #84bc22;
	}

	#menu-nav a.nav-link {
		margin-top: 15px;
		padding-top: 17px;
		height: 66px;
		text-transform: uppercase;
		font-size: 15px;
		font-weight: 400;
		font-family:'Times New Roman', Times, serif;
	}

	.navbar .megamenu {
		padding: 30px;
		background-color: #262a32;
		height: 385px;
	}

	.megamenu a {
		text-decoration: none;
		color: #fff;
		line-height: 30px;
		font-size: 15px;
		font-family:'Times New Roman', Times, serif;
	}

	.megamenu h6 {
		color: #fff;
		text-transform: uppercase;
		font-size: 16px;
		font-weight: 200;
	}

	.megamenu ul {
		padding: 0;
	}

	.megamenu img {
		max-width: 270px;
	}

	.prefs .nav-link {
		color: #6d6b6a;
	}

	.actions {
		margin-right: 48px;
	}

	#menu-nav .actions a {
		padding: 0 18px;
		margin-top: 25px;
		color: #6d6b6a;
	}

	.actions i {
		font-size: 23px;
	}

	.bi-person {
		cursor: pointer;
	}

	.notification {
		position: relative;
	}
	.notification-count {
		color: #84bc22;
		position: absolute;
		top: -2px;
		right: 8px;
		border: 1px solid #84bc22;
		border-radius: 50%;
		padding: 2px 5px;
		font-size: 0.5rem;
		background-color: #fff;
	}
</style>
