<script>
	import Navbar from '$lib/Navbar.svelte';
	import Footer from '$lib/Footer.svelte';
	import Benefits from '$lib/Benefits.svelte';
</script>

<Navbar />

<!--carousel banner-->
<section class="carousel-wrapper">
	<div class="carousel-container row">
		<div class="column col-lg-9">
			<img src="static/img/carousel/carouselbanner.png" alt="carousel-banner" />
			<div class="top-left">Control and manage any<br /> device with cloud solutions</div>
			<div class="bottom-left">
				Improve business perfomance and the user experience<br /> with the right mix of IoT technology
				and processes
			</div>
			<div class="bottom-left button btn-view">View more</div>
		</div>
		<div class="sales-container column col-lg-3">
			<img src="static/img/pdp/holidaysattribute.png" alt="holidaysattribute" />
			<div class="top-center">55%</div>
			<div class="bottom-center">Summer<br /> Sales</div>
			<div class="right-center "> Follow us on Facebook</div>
			<div class="bottom-right ">
				Sed ut perspiciatis unde omnis iste <br /> natus error sit voluptatem
			</div>
			<div class="btn-fb">
				<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 320 512"
					><path
						d="M279.14 288l14.22-92.66h-88.91v-60.13c0-25.35 12.42-50.06 52.24-50.06h40.42V6.26S260.43 0 225.36 0c-73.22 0-121.08 44.38-121.08 124.72v70.62H22.89V288h81.39v224h100.17V288z"
					/></svg
				>Follow
			</div>
		</div>
	</div>
</section>

<!--popular items starts here -->
<section class=" popular-items wrapper">
	<div class="row divider">
		<div class="hr" />
		<h4>Popular Items</h4>
		<div class="hr" />
	</div>
	<div class="cards row">
		<div class="column col-3">
			<div class="my-card">
				<img src="static/img/popularitems/popularitems1.png" />
				<p class="card-text">Kristina Dam Oak Table With White Marble Top <br /> $799.55</p>
			</div>
		</div>
		<div class="column col-3">
			<div class="my-card">
				<img src="static/img/popularitems/popularitems2.png" />
				<p class="card-text">Hay-About A Lounge Chair AAL 93</p>
				<div class="btn-group">
					<button type="button" class="btn btn-secondary price">$659.55</button>
					<button type="button" class="btn btn-secondary text-btn">BUY NOW</button>
				</div>
			</div>
		</div>
		<div class="column col-3">
			<div class="my-card card-overlay ">
				<img src="static/img/popularitems/popularitems3.png" />
				<div class="overlay">
					<i class="bi bi-plus" />
					<i class="bi bi-heart-fill" />
				</div>
				<p class="card-text">Activate Facial Mask and Charcoal Soap</p>
			</div>
		</div>
		<div class="column col-3">
			<div class="my-card">
				<img src="static/img/popularitems/popularitems4.png" />
				<p class="card-text">Cocktail Table Walnut <br />|YES <br />$299.99</p>
			</div>
		</div>
	</div>
	<div class="cards row">
		<div class="column col-3">
			<div class="my-card">
				<img src="static/img/popularitems//popularitems5.png" />
				<p class="card-text">Hay-About A Lounge Chair AAL 93 <br />$659.55</p>
			</div>
		</div>
		<div class="column col-3">
			<div class="my-card">
				<img src="static/img/popularitems/popularitems6.png" />
				<p class="card-text">Tory Desk Calendar<br />$410.99</p>
			</div>
		</div>
		<div class="column col-3">
			<div class="my-card">
				<img src="static/img/popularitems/popularitems7.png" />
				<p class="card-text">CH445 Wing Chair on Suite NY <br />$330.55</p>
			</div>
		</div>
		<div class="column col-3">
			<div class="my-card cardx-overlay">
				<img src="static/img/popularitems/popularitems8.png" />
				<p class="card-text last-text">My dragons are misbehaving again.<br />Unbelieveable!</p>
				<div class="overlay" />
			</div>
		</div>
	</div>
	<div class="row">
		<button class="button">Load more</button>
	</div>
</section>

<!--banner osf starts here-->

<div class="row banner-osf" id="box-search">
	<div class="thumbnail text-center">
		<img src="static/img/banner/bannerosf.png" alt="banner" class="img-responsive" />
		<div class="caption">
			<p>Sed out perspiciatis une omnis iste natus error sit volptatem accusantium</p>
		</div>
	</div>
</div>

<!--featured product starts here-->
<section class="featured-product wrapper">
	<div class="row">
		<h3>Featured Product</h3>
		<h6>Unde omnis iste natus error sit voluptatem</h6>
	</div>
	<!--create div for hr, ///, hr-->
	<div class="row slider">
		<a href="#" class="previous round">&#8249;</a>
		<div class="hr" />
		///
		<div class="hr" />
		<a href="#" class="next round">&#8250;</a>
	</div>

	<div class="cards row">
		<div class="column col-3">
			<div class="my-card">
				<img src="static/img/cards/calendar.png" />
				<p class="card-text">Kristina Dam Oak Table With White Marble</p>
				<h5>Awesome</h5>
			</div>
		</div>

		<div class="column col-3">
			<div class="my-card">
				<img src="static/img/cards/gracioushome.png" />
				<p class="card-text">Kristina Dam Oak Table With White Marble</p>
				<h5>Marketing</h5>
			</div>
		</div>

		<div class="column col-3">
			<div class="my-card">
				<img src="static/img/cards/pen.png" />
				<p class="card-text">Kristina Dam Oak Table With White Marble</p>
				<h5>Awesome</h5>
			</div>
		</div>

		<div class="column col-3">
			<div class="my-card">
				<img src="static/img/cards/salesforce.png" />
				<p class="card-text">Kristina Dam Oak Table With White Marble</p>
				<h5>Marketing</h5>
			</div>
		</div>
	</div>
</section>

<Benefits />
<Footer />

<style>
	/*banner osf*/
	.banner-osf {
		max-width: 100%;
		height: 445px;
	}
	.thumbnail {
		position: relative;
	}

	.caption {
		position: absolute;
		top: 45%;
		left: 0;
		width: 100%;
		color: #ffffff;
	}
	/*featured product */
	.featured-product {
		background-color: #262a32;
		max-width: 100%;
		height: 550px;
	}

	.featured-product h3 {
		color: #ffffff;
		text-align: center;
		margin-top: 30px;
	}
	.featured-product h6 {
		color: #ffffff;
		text-align: center;
	}
	.hr {
		display: inline-block;
		border-top: 1px solid #ffffff;
		width: 235px;
		margin: 17px;
	}
	.slider {
		justify-content: center;
		margin-left: -9px;
		color: #ffffff;
	}
	.slider a {
		text-decoration: none;
		display: inline-block;
	}
	.previous {
		width: 30px;
		height: 30px;
		color: rgb(253, 253, 253);
		background-color: #2d343a;
		margin-top: -5px;
	}

	.next {
		width: 30px;
		height: 30px;
		color: rgb(255, 255, 255);
		background-color: #2d343a;
		margin-top: -5px;
	}

	.round {
		border-radius: 10%;
	}
	.my-card {
		border-radius: 5px;
		overflow: hidden;
		background: white;
		width: 230px;
		margin-top: 40px;
		margin-left: 50px;
		margin-right: 12px;
		align-self: center;
	}

	.card-text {
		text-align: center;
		font-family: Lato, sans-serif;
		font-size: 20px;
	}
	.my-card h5 {
		color: #84bc22;
		text-align: center;
		font-family: Lato ExtraBold, sans-serif;
		font-size: 18px;
	}
	/*popular items*/
	.card-overlay {
		position: relative;
		width: 50%;
	}
	.overlay {
		position: absolute;
		top: 0;
		height: 100%;
		width: 100%;
		opacity: 0;
		transition: 0.1s linear;
		background-color: rgba(53, 202, 126, 0.8);
	}

	.overlay i {
		border-radius: 50%;
		font-size: 3rem;
		width: 70px;
		height: 70px;
		display: inline-block;
		background-color: white;
	}

	.overlay .bi-plus {
		color: #23c46e;
		margin-left: 40px;
		margin-top: 140px;
		padding: 0px 10px;
	}
	.overlay .bi-heart-fill {
		color: #e73c68;
		margin-top: 140px;
		margin-left: 15px;
		padding: 0px 10px;
	}
	.card-overlay:hover .overlay {
		opacity: 1;
	}
	.cardx-overlay {
		position: relative;
		width: 50%;
	}
	.cardx-overlay .overlay {
		position: absolute;
		top: 0;
		height: 100%;
		width: 100%;
		opacity: 0;
		transition: 0.1s linear;
		background: rgb(106, 93, 143);
		background: linear-gradient(0deg, rgba(106, 93, 143, 0.8) 0%, rgba(203, 100, 138, 0.8) 100%);
	}
	.cardx-overlay:hover .overlay {
		opacity: 1;
	}

	.popular-items {
		background-color: #262a32;
		max-width: 100%;

		padding-bottom: 50px;
	}
	.popular-items h4 {
		color: #ffffff;
		text-align: center;
		font-family: Lato ExtraBold, sans-serif;
		font: size 20px;
		padding-top: 2px;
		width: fit-content;
	}
	.popular-items .card-text {
		text-align: center;
		font-family: Lato, sans-serif;
		font-size: 15px;
		color: black;
		padding-top: 20px;
	}
	.popular-items .last-text {
		margin-top: -200px;
		color: #ffffff;
	}
	.popular-items .my-card {
		border-radius: 5px;
		overflow: hidden;
		background: white;
		width: 240px;
		height: 340px;
		margin-top: 40px;
		margin-left: 35px;
		margin-right: 12px;
		align-self: center;
	}
	.popular-items .column {
		margin-right: -85px;
		margin-left: 50px;
	}

	.popular-items .button {
		margin-top: 50px;
		margin-left: 500px;
		margin-right: 500px;
		margin-bottom: 45px;
		background-color: #262a32;
		color: #ffffff;
		padding: 10px 20px;
		text-align: center;
		text-decoration: none;
		display: inline-block;
		cursor: pointer;
		border-radius: 16px;
		width: 250px;
		font-size: 18px;
	}

	.popular-items .btn-group {
		padding-left: 25px;
		padding-right: 0px;
		padding-bottom: 25px;
		text-align: center;
		text-decoration: none;
		display: inline-block;
		margin: -25px 2px;
		cursor: pointer;
		border-radius: 16px;
		font-size: 14px;
	}
	.price {
		color: #84bc22;
		background-color: #ffffff;
		border-radius: 16px;
	}
	.text-btn {
		color: black;
		background-color: #ffffff;

		border-top-left-radius: 0px;
		border-bottom-left-radius: 0;
		border-top-right-radius: 16px;
		border-bottom-right-radius: 16px;
		margin-left: -4px;
	}

	.popular-items .hr {
		border-top: 2px solid #3c4047;
		width: 400px;
	}
	.divider {
		padding: 60px 53px 50px 53px;
		align-self: center;
		margin-left: 25px;
	}
	/*carousel-banner*/
	.carousel-container {
		position: relative;
		width: 100%;
		margin-bottom: 30px;
		margin-right: 50px;
		margin-left: 20px;
	}
	.bottom-left {
		position: absolute;
		bottom: 175px;
		left: 70px;
		color: #ffffff;
		font-family: Lato Regular;
		font-size: 15px;
	}

	.top-left {
		position: absolute;
		top: 65px;
		left: 70px;
		color: #ffffff;
		font-family: Myriad Pro;
		font-weight: bold;
		font-size: 40px;
	}
	.btn-view {
		background-color: none;
		border: 1px solid #ffffff;
		color: #ffffff;
		padding: 10px 20px;
		text-align: center;
		text-decoration: none;
		text-transform: uppercase;
		display: inline-block;
		margin: -100px 15px;
		cursor: pointer;
		border-radius: 16px;
	}
	/*sales wraper*/
	.sales-container {
		position: relative;
		padding-left: 0px;
	}
	.top-center {
		position: absolute;
		top: 5%;
		left: 13%;
		color: #ffffff;
		font-size: 100px;
		font-family: Lato;
		font-weight: bold;
	}
	.bottom-center {
		position: absolute;
		top: 40%;
		left: 20%;
		color: #ffffff;
		font-size: 32px;
		font-family: Lato;
		text-transform: uppercase;
		text-align: center;
	}
	.right-center {
		position: absolute;
		top: 69%;
		left: 6%;
		color: #45413e;
		font-size: 24px;
		font-family: Lato;
		text-align: center;
	}
	.bottom-right {
		position: absolute;
		top: 77%;
		left: 8%;
		color: #45413e;
		font-size: 15px;
		font-family: Lato;
		text-align: center;
	}
	.btn-fb {
		background-color: none;
		border: 2px solid #3b5998;
		color: #3b5998;
		padding: 9px 5px;
		text-align: center;
		text-decoration: none;
		width: 140px;
		height: 40px;
		display: inline-block;
		margin-top: 125px;
		margin-left: 55px;
		cursor: pointer;
		border-radius: 20px;
		text-transform: uppercase;
		text-align: center;
		font-family: Lato;
		font-size: 14px;
	}

	.btn-fb svg {
		height: 100%;
		fill: #3b5998;
		float: left;
		padding-left: 14px;
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
