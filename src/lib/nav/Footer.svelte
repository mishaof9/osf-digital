<script>
	import Social from '$lib/Social.svelte';
	import Login from '$lib/modals/Login.svelte';

	let show_login = false;
</script>

{#if show_login}
	<Login on:close={() => (show_login = false)} />
{/if}

<!--footer starts here-->
<footer>
	<div class="container-fluid">
		<div class="row">
			<div class="col-2">
				<small
					>&copy; Copyright {new Date().getFullYear()}.<br />
					All rights reserved.</small
				>
				<p><strong>Contact</strong></p>
				<p>
					Headquarters <br />
					5600, Blvd. des Galeries, Bur 530 <br />
					Quebec,Quebec G2K 2H6.
				</p>
				<p><a href="mailto:contact@osf-global.com" id="mail">contact@osf-global.com</a></p>
				<p><a href="tel:+1(888)548-4333" id="phone">+1(888)548-4333 </a></p>
			</div>
			<div class="col-2">
				<ul class="list-unstyled">
					<li>
						<p><strong>Categories</strong></p>
					</li>
					<li>
						<p><a href="/404">Alcohol </a></p>
					</li>
					<li>
						<p><a href="/404">Art </a></p>
					</li>
					<li>
						<p><a href="/404">Books </a></p>
					</li>
					<li>
						<p><a href="/404">Drink </a></p>
					</li>
					<li>
						<p><a href="/404">Electronics </a></p>
					</li>
				</ul>
			</div>
			<div class="col-2 second">
				<ul class="list-unstyled">
					<li>
						<p />

						<p><a href="/404">Home </a></p>
					</li>
					<li>
						<p><a href="/404">Jewelry </a></p>
					</li>
					<li>
						<p><a href="/404">Kids &amp; Baby </a></p>
					</li>
					<li>
						<p><a href="/404">Men's Fashion </a></p>
					</li>
					<li>
						<p><a href="/404">Mobile </a></p>
					</li>
					<li>
						<p><a href="/404">Motorcycles </a></p>
					</li>
					<li>
						<p><a href="/404">Movies </a></p>
					</li>
					<li>
						<p><a href="/404">Music </a></p>
					</li>
				</ul>
			</div>
			<div class="col-2 third">
				<ul class="list-unstyled">
					<li>
						<p><a href="/404">Sport </a></p>
					</li>
					<li>
						<p><a href="/404">Toys </a></p>
					</li>
					<li>
						<p><a href="/404">Travel </a></p>
					</li>
					<li>
						<p><a href="/404">Women's Fashion</a></p>
					</li>
				</ul>
			</div>
			<div class="col-2">
				<ul class="list-unstyled">
					<li>
						<p><strong>About</strong></p>
					</li>
					<li>
						<p><a href="/404">About us </a></p>
					</li>
					<li>
						<p><a href="/404">Delivery </a></p>
					</li>
					<li>
						<p><a href="/404">Testimonials </a></p>
					</li>
					<li>
						<p><a href="/404">Contact </a></p>
					</li>
				</ul>
			</div>
			<div class="col-2">
				<Social />
			</div>
		</div>
	</div>
</footer>
<section class="second-nav">
	<ul class="nav justify-content-center d-md-none ">
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
</section>

<style>
	/* footer*/
	footer {
		font-size: 13pt;
		display: flex;
		max-width: 100%;
		position: sticky;
		flex-flow: column;
		text-decoration: none;
		padding-top: 30px;
		padding-left: 50px;
	}
	footer .second {
		padding-top: 25px;
	}
	footer .third {
		padding-top: 40px;
	}
	footer a {
		text-decoration: none;
		color: #b1afae;
	}

	#mail,
	#phone {
		color: black;
	}

	/*section from navbar*/
	.second-nav {
		background-color: #262a32;
	}
	.nav-item {
		font-size: 19px;
		padding: 0px 10px;
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
	.nav-item a {
		color: #8e9196;
	}
	.bi-person {
		cursor: pointer;
	}
	/* we need :global here so svelte doesn't remove this css rule */
	.nav-item > :global(a.show) {
		color: #ffffff;
		background-color: #262a32;
	}
</style>
