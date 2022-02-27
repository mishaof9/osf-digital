<script>
	import Benefits from '$lib/Benefits.svelte';
	import ProductCard from '$lib/cards/ProductCard.svelte';
	import DragonsMisbeaving from '$lib/cards/DragonsMisbeaving.svelte';
	import FeaturedProduct from '$lib/FeaturedProduct.svelte';
	import PopularItems from '$lib/PopularItems.svelte';

	let popular_items = [
		{
			component: ProductCard,
			image: '/static/img/popularitems/item1.png',
			name: 'Kristina Dam Oak Table With White Marble Top',
			price: '799.55'
		},
		{
			component: ProductCard,
			image: '/static/img/popularitems/item2.png',
			name: 'Hay-About A Lounge Chair AAL 93',
			price: '659.55',
			discounted: true
		},
		{
			component: ProductCard,
			image: '/static/img/popularitems/item3.png',
			name: 'Activate Facial Mask and Charcoal Soap',
			price: '129.55'
		},
		{
			component: ProductCard,
			image: '/static/img/popularitems/item4.png',
			name: 'Cocktail Table Walnut',
			price: '629.99'
		},
		{
			component: ProductCard,
			image: '/static/img/popularitems/item5.png',
			name: 'Hay-About A Lounge Chair AAL 93',
			price: '659.55'
		},
		{
			component: ProductCard,
			image: '/static/img/popularitems/item6.png',
			name: 'Tory Desk Calendar',
			price: '410.99',
			discounted: true
		},
		{
			component: ProductCard,
			image: '/static/img/popularitems/item7.png',
			name: 'CH445 Wing Chair on Suite NY',
			price: '330.55'
		},
		{
			component: DragonsMisbeaving
		}
	];
	function loadMore() {
		let product = {
			component: ProductCard,
			image: 'static/img/popularitems/item5.png',
			name: 'Hay-About A Launge Chair AAL 93',
			price: '695.55'
		};
		popular_items.push(product);

		// we need so svelte can tell that we modified the array
		popular_items = popular_items;
	}
</script>

<!--carousel banner-->
<section class="carousel-container row d-none d-md-flex">
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

	<div class="sales-container column col-lg-3 d-none d-lg-block">
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
		<div class="col">
			<div class="hr" />
		</div>
		<div class="col col-auto">
			<h4>Popular Items</h4>
		</div>
		<div class="col">
			<div class="hr" />
		</div>
	</div>

	<PopularItems items={popular_items} />

    <div class="text-center">
        <button class="button" on:click={loadMore}>Load more</button>
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

<FeaturedProduct />

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
		margin-top: 15px;
	}

	.divider {
		margin: 0 2.5%;
		padding-top: 40px;
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
