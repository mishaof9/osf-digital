<script>
	import Benefits from '$lib/Benefits.svelte';
	import CardRow from '$lib/CardRow.svelte';
	import Card from '$lib/Card.svelte';
	import ProductCard from '$lib/ProductCard.svelte';
	import DragonsMisbeaving from '$lib/DragonsMisbeaving.svelte';
</script>

<!--carousel banner-->
<section class="carousel-container row">
	<div
		id="carouselExampleCaptions"
		class="carousel slide col-lg-9"
		data-bs-ride="false"
		data-bs-interval="false"
	>
		<div class="carousel-indicators">
			<button
				type="button"
				data-bs-target="#carouselExampleCaptions"
				data-bs-slide-to="0"
				class="active"
				aria-current="true"
				aria-label="Slide 1"
			/>
			<button
				type="button"
				data-bs-target="#carouselExampleCaptions"
				data-bs-slide-to="1"
				aria-label="Slide 2"
			/>
			<button
				type="button"
				data-bs-target="#carouselExampleCaptions"
				data-bs-slide-to="2"
				aria-label="Slide 3"
			/>
		</div>
		<div class="carousel-inner">
			<div class="carousel-item active first-slide">
				<img src="static/img/carousel/carousel.png" class="d-block w-100" alt="carousel-center" />
				<div class="carousel-text d-none d-md-block">
					<h5>Control and manage any<br /> device with cloud solutions</h5>
					<p>
						Improve business perfomance and the user experience<br /> with the right mix of IoT technology
						and processes.
					</p>
					<div class="bottom-left button btn-view">View more</div>
				</div>
			</div>
			<div class="carousel-item second-slide">
				<img
					src="static/img/carousel/carousel-center.jpg"
					class="d-block w-100"
					alt="carousel-center"
				/>
				<div class="carousel-text d-none d-md-block">
					<h5>Control and manage any<br /> device with cloud solutions</h5>
					<p>
						Improve business perfomance and the user experience<br /> with the right mix of IoT technology
						and processes.
					</p>
					<div class="bottom-left button btn-view">View more</div>
				</div>
			</div>
			<div class="carousel-item third-slide">
				<img src="static/img/carousel/slider3.jpg" class="d-block w-100" alt="carousel-right" />
				<div class="carousel-text d-none d-md-block">
					<h5>Control and manage any<br /> device with cloud solutions</h5>
					<p>
						Improve business perfomance and the user experience<br /> with the right mix of IoT technology
						and processes.
					</p>
					<div class="button btn-view">View more</div>
				</div>
			</div>
		</div>
		<button
			class="carousel-control-prev"
			type="button"
			data-bs-target="#carouselExampleCaptions"
			data-bs-slide="prev"
		/>
		<button
			class="carousel-control-next"
			type="button"
			data-bs-target="#carouselExampleCaptions"
			data-bs-slide="next"
		/>
	</div>

	<div class="sales-container column col-lg-3">
		<img src="static/img/pdp/holidaysattribute.png" alt="holidaysattribute" />
		<div class="top-center">55%</div>
		<div class="bottom-center">Summer<br /> Sales</div>
		<div class="right-center ">Follow us on Facebook</div>
		<div class="bottom-right ">
			Sed ut perspiciatis unde omnis iste <br /> natus error sit voluptatem
		</div>
		<div class="btn-fb">
			<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 320 512"
				><path
					d="M279.14 288l14.22-92.66h-88.91v-60.13c0-25.35 12.42-50.06 52.24-50.06h40.42V6.26S260.43 0 225.36 0c-73.22 0-121.08 44.38-121.08 124.72v70.62H22.89V288h81.39v224h100.17V288z"
				/></svg
			> <a href="https://www.facebook.com/OSFDigital/">Follow</a>
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
	<CardRow>
		<ProductCard
			name="Kristina Dam Oak Table With White Marble Top"
			img="static/img/popularitems/item1.png"
			price="799.55"
		/>
		<ProductCard
			name="Hay-About A Lounge Chair AAL 93"
			img="static/img/popularitems/item2.png"
			price="659.55"
			discounted={true}
		/>
		<ProductCard
			name="Activate Facial Mask and Charcoal Soap"
			img="static/img/popularitems/item3.png"
			price="129.55"
		/>
		<ProductCard
			name="Cocktail Table Walnut"
			img="static/img/popularitems/item4.png"
			price="299.99"
		/>
	</CardRow>
	<CardRow>
		<ProductCard
			name="Hay-About A Lounge Chair AAL 93"
			img="static/img/popularitems/item5.png"
			price="659.55"
		/>
		<ProductCard
			name="Tory Desk Calendar"
			img="static/img/popularitems/item6.png"
			price="410.99"
			discounted={true}
		/>
		<ProductCard
			name="CH445 Wing Chair on Suite NY"
			img="static/img/popularitems/item7.png"
			price="330.55"
		/>
		<DragonsMisbeaving />
	</CardRow>

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

	<CardRow>
		<Card height="295">
			<div class="featured">
				<img src="static/img/cards/calendar.png" />
				<p>Kristina Dam Oak Table With White Marble</p>
				<h5>Awesome</h5>
			</div>
		</Card>
		<Card height="295">
			<div class="featured">
				<img src="static/img/cards/gracioushome.png" />
				<p class="card-text">Kristina Dam Oak Table With White Marble</p>
				<h5>Marketing</h5>
			</div>
		</Card>
		<Card height="295">
			<div class="featured">
				<img src="static/img/cards/pen.png" />
				<p>Kristina Dam Oak Table With White Marble</p>
				<h5>Awesome</h5>
			</div>
		</Card>
		<Card height="295">
			<div class="featured">
				<img src="static/img/cards/salesforce.png" />
				<p>Kristina Dam Oak Table With White Marble</p>
				<h5>Marketing</h5>
			</div>
		</Card>
	</CardRow>
</section>

<Benefits />

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

	.featured p {
		text-align: center;
		font-size: 20px;
	}
	.featured h5 {
		color: #84bc22;
		text-align: center;
		font-family: Lato ExtraBold, sans-serif;
		font-size: 18px;
	}
	/*popular items*/

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

	.carousel-item h5 {
		font-family: Myriad Pro;
		font-weight: bold;
		font-size: 50px;
	}
	.carousel-item p {
		font-family: Myriad Pro;
		font-size: 18px;
	}
	.carousel-item img {
		width: 807px;
		height: 505px;
	}
	.first-slide .carousel-text {
		position: absolute;
		top: 80px;
		left: 60px;
		color: #ffffff;
	}
	.first-slide .carousel-text h5 {
		margin-bottom: 90x;
	}
	.first-slide .carousel-text .btn-view {
		margin-top: 50px;
	}
	.second-slide .carousel-text {
		position: absolute;
		top: 80px;
		left: 150px;
		color: #ffffff;
		text-align: center;
	}
	.second-slide .carousel-text h5 {
		margin-bottom: 100px;
	}
	.second-slide .carousel-text .btn-view {
		margin-top: 30px;
		margin-left: -60px;
	}
	.third-slide .carousel-text {
		position: absolute;
		top: 80px;
		right: 75px;
		color: #ffffff;
		text-align: right;
	}
	.third-slide .carousel-text h5 {
		margin-bottom: 100px;
	}
	.third-slide .carousel-text .btn-view {
		margin-top: 30px;
		right: 0px;
	}
	.carousel-container {
		position: relative;
		padding: 26px 56px;
        background-color: #ffffff;
	}

    .carousel-indicators button {
        border-radius: 50%;
        width: 5px;
        height: 5px;
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
		position: absolute;
        font-family: Lato Regular;
		font-size: 15px;
		cursor: pointer;
		border-radius: 16px;
	}
	/*sales wraper*/
	.sales-container {
		position: relative;
		padding-left: 20px;
	}
	.top-center {
		position: absolute;
		top: 5%;
		left: 13%;
		color: #ffffff;
		font-size: 100px;
		font-weight: bold;
	}
	.bottom-center {
		position: absolute;
		top: 40%;
		left: 20%;
		color: #ffffff;
		font-size: 32px;
		text-transform: uppercase;
		text-align: center;
	}
	.right-center {
		position: absolute;
		top: 69%;
		left: 8%;
		color: #45413e;
		font-size: 24px;
		text-align: center;
	}
	.bottom-right {
		position: absolute;
		top: 77%;
		left: 8%;
		color: #45413e;
		font-size: 15px;
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
		font-size: 14px;
	}

	.btn-fb svg {
		height: 100%;
		fill: #3b5998;
		float: left;
		padding-left: 14px;
	}
	.btn-fb a {
		text-decoration: none;
		color: #3b5998;
	}
	.btn-fb:hover {
		opacity: 1;
		background-color: #3b5998;
	}
	.btn-fb:hover a {
		color: #ffffff;
	}
	.btn-fb:hover svg {
		fill: #ffffff;
	}
</style>
