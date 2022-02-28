<script>
	import Breadcrumb from '$lib/nav/Breadcrumb.svelte';
	import Breadcrumbs from '$lib/nav/Breadcrumbs.svelte';
</script>

<Breadcrumbs>
	<Breadcrumb href="/" name="OSF Theme" />
	<Breadcrumb name="404" />
</Breadcrumbs>

<h1 class="text-center">404</h1>

<div class="error-page row">
	<div class="col oops">
		<h1>Oops!</h1>
	</div>

	<div class="col info col-12 col-md-auto">
		<h3>Sorry, this page could not be found!</h3>
		<p>
			Aenean commodo ligula eget dolor. Aenean massa. Cum sociis natoque penatibus <br />et magnis
			dis parturient montes, nascetur ridiculus mus.
		</p>
		<p>
			Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula<br />
			eget dolor. Aenean massa.
		</p>
		<a href="/">Go back to Homepage</a>
		<h3>Search our site</h3>
		<div class="search">
			<input type="text" placeholder="SEARCH" />
			<i class="bi bi-search" />
		</div>
	</div>
</div>

<style>
	.error-page {
		background-color: #ffffff;
		margin: 30px 2.5%;
		padding: 20px;
	}

	.oops {
		display: flex;
		align-items: center;
		justify-content: center;
		background: url(static//img/404/oops.png) -100px no-repeat;
	}

	.oops h1 {
		font-size: 100px;
		font-weight: bold;
		color: #84bc22;
	}

	.error-page a {
		text-decoration: none;
		font-size: 17px;
		color: #84bc22;
		font-weight: bold;
	}

	h3 {
		font-size: 26px;
		font-weight: bold;
		padding-bottom: 10px;
	}

	.search {
		position: relative;
		width: 80%;
	}

	.search > input {
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
	.search > input:focus {
		border-color: #45413e;
	}
</style>
