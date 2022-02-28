<script>
	import Social from '$lib/Social.svelte';
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

{#if show_login}
	<Login on:close={() => (show_login = false)} />
{/if}

<!--footer starts here-->
<footer class="container-fluid">
	<!-- full footer, for large screens -->
	<div class="row g-0 d-none d-md-flex">
		<div class="col">
			<small>
				&copy; Copyright {new Date().getFullYear()}.<br />
				All rights reserved.
			</small>
			<p><strong>Contact</strong></p>
			<p>
				Headquarters <br />
				5600, Blvd. des Galeries, Bur 530 <br />
				Quebec,Quebec G2K 2H6.
			</p>
			<p><a href="mailto:contact@osf-global.com" class="mail">contact@osf-global.com</a></p>
			<p><a href="tel:+1(888)548-4333" class="phone">+1(888)548-4333 </a></p>
		</div>
		<div class="col col-6">
			<h6>Categories</h6>
			<div class="row">
				<ul class="col list-unstyled">
					<li><a href="/404">Alcohol </a></li>
					<li><a href="/404">Art </a></li>
					<li><a href="/404">Books </a></li>
					<li><a href="/404">Drink </a></li>
					<li><a href="/404">Electronics </a></li>
				</ul>
				<ul class="col list-unstyled">
					<li><a href="/404">Home </a></li>
					<li><a href="/404">Jewelry </a></li>
					<li><a href="/404">Kids &amp; Baby </a></li>
					<li><a href="/404">Men's Fashion </a></li>
					<li><a href="/404">Mobile </a></li>
					<li><a href="/404">Motorcycles </a></li>
					<li><a href="/404">Movies </a></li>
					<li><a href="/404">Music </a></li>
				</ul>
				<ul class="col list-unstyled">
					<li><a href="/404">Sport </a></li>
					<li><a href="/404">Toys </a></li>
					<li><a href="/404">Travel </a></li>
					<li><a href="/404">Women's Fashion</a></li>
				</ul>
			</div>
		</div>
		<div class="col col-2">
			<h5>About</h5>
			<ul class="list-unstyled">
				<li><p><a href="/404">About us </a></p></li>
				<li><p><a href="/404">Delivery </a></p></li>
				<li><p><a href="/404">Testimonials </a></p></li>
				<li><p><a href="/404">Contact </a></p></li>
			</ul>
		</div>
		<div class="col col-auto">
			<Social />
		</div>
	</div>

	<!-- for smaller screens -->
	<div class="d-md-none">
		<small>
			&copy; Copyright {new Date().getFullYear()}.<br />
			All rights reserved.
		</small>

		<!-- nav for small screens, with accordion -->
		<div class="mt-3 accordion accordion-flush" id="menu-footer">
			<!-- contact -->
			<div class="accordion-item">
				<h2 class="accordion-header" id="hdr-contact">
					<button
						class="accordion-button collapsed"
						type="button"
						data-bs-toggle="collapse"
						data-bs-target="#coll-contact"
						aria-expanded="false"
						aria-controls="coll-contact"
					>
						Contact
					</button>
				</h2>
				<div
					id="coll-contact"
					class="accordion-collapse collapse"
					aria-labelledby="hdr-contact"
					data-bs-parent="#menu-footer"
				>
					<div class="accordion-body">
						<p>
							Headquarters <br />
							5600, Blvd. des Galeries, Bur 530 <br />
							Quebec,Quebec G2K 2H6.
						</p>
						<p><a href="mailto:contact@osf-global.com" class="mail">contact@osf-global.com</a></p>
						<p><a href="tel:+1(888)548-4333" class="phone">+1(888)548-4333 </a></p>
					</div>
				</div>
			</div>

			<div class="accordion-item">
				<h2 class="accordion-header" id="hdr-categories">
					<button
						class="accordion-button collapsed"
						type="button"
						data-bs-toggle="collapse"
						data-bs-target="#coll-categories"
						aria-expanded="false"
						aria-controls="coll-categories"
					>
						Categories
					</button>
				</h2>
				<div
					id="coll-categories"
					class="accordion-collapse collapse"
					aria-labelledby="hdr-categories"
					data-bs-parent="#menu-footer"
				>
					<ul class="accordion-body list-unstyled">
						<li><a href="/404">Alcohol </a></li>
						<li><a href="/404">Art </a></li>
						<li><a href="/404">Books </a></li>
						<li><a href="/404">Drink </a></li>
						<li><a href="/404">Electronics </a></li>
						<li><a href="/404">Home </a></li>
						<li><a href="/404">Jewelry </a></li>
						<li><a href="/404">Kids &amp; Baby </a></li>
						<li><a href="/404">Men's Fashion </a></li>
						<li><a href="/404">Mobile </a></li>
						<li><a href="/404">Motorcycles </a></li>
						<li><a href="/404">Movies </a></li>
						<li><a href="/404">Music </a></li>
						<li><a href="/404">Sport </a></li>
						<li><a href="/404">Toys </a></li>
						<li><a href="/404">Travel </a></li>
						<li><a href="/404">Women's Fashion</a></li>
					</ul>
				</div>
			</div>

			<div class="accordion-item">
				<h2 class="accordion-header" id="hdr-about">
					<button
						class="accordion-button collapsed"
						type="button"
						data-bs-toggle="collapse"
						data-bs-target="#coll-about"
						aria-expanded="false"
						aria-controls="coll-about"
					>
						About
					</button>
				</h2>
				<div
					id="coll-about"
					class="accordion-collapse collapse"
					aria-labelledby="hdr-about"
					data-bs-parent="#menu-footer"
				>
					<ul class="accordion-body list-unstyled">
						<li><p><a href="/404">About us </a></p></li>
						<li><p><a href="/404">Delivery </a></p></li>
						<li><p><a href="/404">Testimonials </a></p></li>
						<li><p><a href="/404">Contact </a></p></li>
					</ul>
				</div>
			</div>

			<div class="pt-2 pb-4 d-flex justify-content-center">
				<Social />
			</div>
		</div>

	</div>
	<div class="actions d-flex d-md-none justify-content-center">
		<a href=""> <i class="bi bi-search" /></a>
		<a on:click={() => (show_login = true)}> <i class="bi bi-person" /></a>
		
		<a class="notification" href="#">
			<i class="bi bi-heart" />
			<span class="notification-count">1</span></a
		>
		
		<a class="notification" href="#">
			<i class="bi bi-bag" />
			<span class="notification-count">2</span>
		</a>
	</div>
</footer>

<style>
	footer {
		padding: 0;
		background-color: #fff;
	}

	footer > div {
		padding: 0 4%;
		padding-top: 30px;
	}

	footer a {
		text-decoration: none;
		color: #7c7a78;
	}

	.mail,
	.phone {
		color: black;
	}

	.accordion-item {
		border: none;
	}

	.accordion-button {
		border: none;
		box-shadow: none;
		background-color: #fff;
		color: black;
		text-transform: uppercase;
		padding-left: 0;
		padding-right: 0;
	}

	.accordion-button:after {
		font-family: bootstrap-icons !important;
		content: '\F22C';
		background: none;
	}

	.actions {
		background-color: #262a32;
		padding: 0;
	}

	.actions a {
		display: inline-block;
		padding: 19px 18px;
		color: #a8a6a5;
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
		top: 15px;
		right: 8px;
		border: 1px solid #84bc22;
		border-radius: 50%;
		padding: 2px 5px;
		font-size: 0.5rem;
		background-color: #fff;
	}
</style>
