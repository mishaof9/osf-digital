<script>
	import Benefits from '$lib/Benefits.svelte';
	import ProductCard from '$lib/cards/ProductCard.svelte';
	import DragonsMisbeaving from '$lib/cards/DragonsMisbeaving.svelte';
	import FeaturedProduct from '$lib/FeaturedProduct.svelte';
	import PopularItems from '$lib/Products.svelte';

	let popular_items = [
		{
			component: ProductCard,
			image: '/img/popularitems/item1.png',
			name: 'Kristina Dam Oak Table With White Marble Top',
			price: '799.55'
		},
		{
			component: ProductCard,
			image: '/img/popularitems/item2.png',
			name: 'Hay-About A Lounge Chair AAL 93',
			price: '659.55',
			discounted: true
		},
		{
			component: ProductCard,
			image: '/img/popularitems/item3.png',
			name: 'Activate Facial Mask and Charcoal Soap',
			price: '129.55'
		},
		{
			component: ProductCard,
			image: '/img/popularitems/item4.png',
			name: 'Cocktail Table Walnut',
			price: '629.99'
		},
		{
			component: ProductCard,
			image: '/img/popularitems/item5.png',
			name: 'Hay-About A Lounge Chair AAL 93',
			price: '659.55'
		},
		{
			component: ProductCard,
			image: '/img/popularitems/item6.png',
			name: 'Tory Desk Calendar',
			price: '410.99',
			discounted: true
		},
		{
			component: ProductCard,
			image: '/img/popularitems/item7.png',
			name: 'CH445 Wing Chair on Suite NY',
			price: '330.55'
		},
		{
			component: DragonsMisbeaving
		}
	];

	async function loadMore() {
		const resp = await fetch('/products.json');
		let more_products = await resp.json();

		for (let i = 0; i < more_products.length; i++) {
			more_products[i].component = ProductCard;
		}

		popular_items = popular_items.concat(more_products);
	}
</script>

<!--carousel banner-->
<section class="carousel-container row g-0">
	<div id="main-carousel" class="carousel slide col" data-bs-ride="false" data-bs-interval="false">
		<div class="carousel-indicators">
			<button
				type="button"
				data-bs-target="#main-carousel"
				data-bs-slide-to="0"
				class="active"
				aria-current="true"
				aria-label="Slide 1"
			/>
			<button
				type="button"
				data-bs-target="#main-carousel"
				data-bs-slide-to="1"
				aria-label="Slide 2"
			/>
			<button
				type="button"
				data-bs-target="#main-carousel"
				data-bs-slide-to="2"
				aria-label="Slide 3"
			/>
		</div>
		<div class="carousel-inner">
			<div class="carousel-item active">
				<img src="/img/carousel/carousel.png" alt="carousel-center" />
				<div class="w-100">
					<h5 class="fs-3">Control and manage any device with cloud solutions</h5>
					<p>
						Improve business perfomance and the user experience with the right mix of IoT technology
						and processes.
					</p>
					<div class="view-more">
						<a href="/category" class="mx-auto ms-sm-5">View more</a>
					</div>
				</div>
			</div>
			<div class="carousel-item">
				<img src="/img/carousel/carousel-center.jpg" alt="carousel-center" />
				<div>
					<h5 class="fs-3 mx-auto text-center">
						Control and manage any device with cloud solutions
					</h5>
					<p class="mx-auto text-center">
						Improve business perfomance and the user experience with the right mix of IoT technology
						and processes.
					</p>
					<div class="view-more">
						<a href="/category" class="mx-auto">View more</a>
					</div>
				</div>
			</div>
			<div class="carousel-item">
				<img src="/img/carousel/slider3.jpg" alt="carousel-right" />
				<div>
					<h5 class="fs-3 ms-auto text-end">Control and manage any device with cloud solutions</h5>
					<p class="ms-auto text-end">
						Improve business perfomance and the user experience with the right mix of IoT technology
						and processes.
					</p>
					<div class="view-more">
						<a href="/category" class="mx-auto me-sm-5">View more</a>
					</div>
				</div>
			</div>
		</div>
		<button
			class="carousel-control-prev"
			type="button"
			data-bs-target="#main-carousel"
			data-bs-slide="prev"
		/>
		<button
			class="carousel-control-next"
			type="button"
			data-bs-target="#main-carousel"
			data-bs-slide="next"
		/>
	</div>

	<div class="sales col col-lg-auto d-none d-lg-block">
		<div class="discount">
			<h1>55%</h1>
			<h2>Summer Sales</h2>
		</div>

		<h5>Follow us on Facebook</h5>
		<p>Sed ut perspiciatis unde omnis iste <br /> natus error sit voluptatem</p>

		<a href="https://www.facebook.com/OSFDigital/" target="_blank">
			<i class="bi bi-facebook" /> Follow
		</a>
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

	<div class="text-center d-none d-lg-block">
		<button on:click={loadMore}>Load more <i class="bi bi-arrow-clockwise" /></button>
	</div>
</section>

<!--banner osf starts here-->
<div class="banner-osf">
	<p>Sed out perspiciatis une omnis iste natus error sit volptatem accusantium</p>
</div>

<FeaturedProduct />

<Benefits />

<style>
	/*banner osf*/
	.banner-osf {
		background: url(/img/banner/bannerosf.png) center no-repeat;
		background-color: #262a32;
		height: 445px;
		color: #fff;
		display: flex;
		align-items: center;
		justify-content: center;
	}

	/*popular items*/

	.popular-items {
		background-color: #262a32;
		max-width: 100%;
		padding-bottom: 50px;
	}
	.popular-items h4 {
		color: #fff;
		text-align: center;
		font-family: Lato ExtraBold, sans-serif;
		font: size 20px;
		padding-top: 2px;
		width: fit-content;
	}

	.popular-items button {
		display: inline-block;
		margin-top: 50px;
		margin-bottom: 45px;
		border: 2px solid #fff;
		border-radius: 25px;
		padding: 10px 100px;
		background-color: #262a32;
		text-transform: uppercase;
		color: #fff;
		font-size: 18px;
	}
	.popular-items button i {
		margin-left: 20px;
	}

	.popular-items .hr {
		border-top: 2px solid #3c4047;
		margin-top: 15px;
	}

	.divider {
		margin: 0 2.5%;
		padding-top: 40px;
		margin-bottom: 20px;
	}
	/*carousel-banner*/
	.carousel-container {
		position: relative;
		padding: 26px 2.5%;
		background-color: #ffffff;
	}

	.carousel-indicators button {
		border-radius: 50%;
		width: 5px;
		height: 5px;
	}

	.carousel-item {
		height: 505px;
		color: #fff;
		max-width: 1170px;
	}

	.carousel-item img {
		position: absolute;
		right: 0;
		height: 100%;
	}

	.carousel-item > div {
		position: absolute;
		top: 0;
		left: 0;
		height: 100%;
		width: 100%;
	}

	.carousel-item h5 {
		font-family: Myriad Pro;
		font-weight: bold;
		padding: 5% 4%;
		max-width: 650px;
	}
	.carousel-item p {
		box-sizing: content-box;
		font-family: Myriad Pro;
		padding: 5% 5%;
		max-width: 530px;
	}

	.carousel-item .view-more {
		position: absolute;
		width: 100%;
		bottom: 70px;
	}

	.carousel-item a {
		display: block;
		width: fit-content;
		border-radius: 16px;
		padding: 10px 20px;
		background-color: inherit;
		border: 1px solid #fff;
		color: #fff;
		text-align: center;
		text-decoration: none;
		text-transform: uppercase;
		font-family: Lato Regular;
		font-size: 15px;
		cursor: pointer;
	}

	.sales {
		text-align: center;
	}

	.discount {
		background-image: url(/img/pdp/holidaysattribute.png);
		width: 270px;
		height: 335px;
		padding-top: 50px;
		color: #fff;
		margin-bottom: 30px;
	}

	.discount h1 {
		font-weight: bolder;
		font-size: 80px;
	}

	.discount h2 {
		margin: 0 auto;
		margin-top: 70px;
		text-transform: uppercase;
		width: 50%;
	}

	.sales h5 {
		font-size: 18px;
	}

	.sales p {
		font-size: 14px;
	}

	.sales a {
		display: inline-block;
		width: 140px;
		height: 40px;
		padding: 9px 5px;
		border: 2px solid #3b5998;
		border-radius: 20px;
		margin-top: 10px;
		color: #3b5998;
		text-decoration: none;
		text-transform: uppercase;
		text-align: center;
		font-size: 14px;
	}

	.sales i {
		margin-right: 15px;
	}
</style>
