<script>
	import Login from '$lib/Login.svelte';
	let showLogin = false;
</script>

<Login bind:show={showLogin} />

<!--navbar starting here-->

<div class="nav-container mx-auto">
	<nav class="navbar navbar-expand-lg navbar-light ">
		<div class="container osf-logo">
			<img src="static/img/logo/logoosf.png" alt="logo" />
			<div class="text-sm-center">
				<h4 class="osf">OSF</h4>
				<h4 class="academy">Academy</h4>
			</div>
		</div>
		<div class="collapse navbar-collapse" id="navbarNavDropdown">
			<ul class="navbar-nav">
				<li class="nav-item dropdown mx-2">
					<a
						class="nav-link dropdown-toggle"
						href="#"
						id="navbarDropdownMenuLink"
						role="button"
						data-toggle="dropdown"
						aria-haspopup="true"
						aria-expanded="false"
					>
						Services
					</a>
					<div class="dropdown-menu" aria-labelledby="navbarDropdownMenuLink">
						<a class="dropdown-item" href="#">Action</a>
						<a class="dropdown-item" href="#">Another action</a>
						<a class="dropdown-item" href="#">Something else here</a>
					</div>
				</li>
				<li class="nav-item active mx-2">
					<a class="nav-link" href="#">Company <span class="sr-only" /></a>
				</li>
				<li class="nav-item mx-3">
					<a class="nav-link" href="#">Library</a>
				</li>
				<li class="nav-item mx-3">
					<a class="nav-link" href="#">Contact Us</a>
				</li>
				<li class="nav-item dropdown mx-2 language ">
					<a
						class="nav-link dropdown-toggle"
						href="#"
						id="navbarDropdownMenuLink"
						role="button"
						data-toggle="dropdown"
						aria-haspopup="true"
						aria-expanded="false"
					>
						EN
					</a>
					<div class="dropdown-menu" aria-labelledby="navbarDropdownMenuLink">
						<a class="dropdown-item" href="#">FR</a>
						<a class="dropdown-item" href="#">IT</a>
						<a class="dropdown-item" href="#">Ro</a>
					</div>
				</li>
				<li class="nav-item dropdown mx-2 money-open">
					<a
						class="nav-link dropdown-toggle"
						href="#"
						id="navbarDropdownMenuLink"
						role="button"
						data-toggle="dropdown"
						aria-haspopup="true"
						aria-expanded="false"
					>
						$ US
					</a>
					<div class="dropdown-menu" aria-labelledby="navbarDropdownMenuLink">
						<a class="dropdown-item" href="#">EUR</a>
						<a class="dropdown-item" href="#">BTC</a>
						<a class="dropdown-item" href="#">GBP</a>
					</div>
				</li>
				<li class="nav-item mx-2">
					<a class="nav-link" href="#"><i class="bi bi-search" /></a>
				</li>
				<li class="nav-item mx-2">
					<a class="nav-link" on:click={() => (showLogin = true)}><i class="bi bi-person" /></a>
				</li>

				<li class="nav-item mx-2 notification">
					<a class="nav-link" href="#"><i class="bi bi-heart" /></a>
					<span class="notification-count">1</span>
				</li>
				<li class="nav-item mx-2 notification">
					<a class="nav-link" href="#"><i class="bi bi-bag" /></a>
					<span class="notification-count">2</span>
				</li>
			</ul>
		</div>
	</nav>
</div>

<!--end of navbar-->
<style>
	h4 {
		font-family: 'Lato', sans-serif;
		text-align: center;
	}
	.osf-logo {
		width: 200px;
		margin-top: 1.5rem;
		margin-right: 256px;
		margin-left: -16px;
	}

	.osf-logo img {
		float: left;
		margin-bottom: 0.5rem;
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
	.nav-container {
		display: flex;
		width: 100%;
		position: relative;
		justify-content: center;
		vertical-align: top;
		align-items: baseline;
		margin-top: 1.5rem;

		row-gap: 10px;
		column-gap: 20px;
	}
	.nav-item {
		font-family: Lato, sans-serif;
		font: size 19px;
	}
	.notification{
		
		position:relative;

	}
	.notification-count {
		color:#84bc22;
		position:absolute;
		top:0px;
		right:-2px;
		border:1px solid #84bc22;
		border-radius:50%;
		padding:2px 5px;
		font-size: 0.5rem;
		background-color: #fff;

	}
</style>
