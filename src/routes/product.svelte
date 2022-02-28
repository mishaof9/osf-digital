<script>
	import Benefits from '$lib/Benefits.svelte';
	import ProductCard from '$lib/cards/ProductCard.svelte';
	import Breadcrumbs from '$lib/nav/Breadcrumbs.svelte';
	import Breadcrumb from '$lib/nav/Breadcrumb.svelte';
	import Social from '$lib/Social.svelte';
	import PopularItems from '$lib/Products.svelte';

	function chunk(arr, len) {
		var chunks = [],
			i = 0,
			n = arr.length;
		while (i < n) {
			chunks.push(arr.slice(i, (i += len)));
		}
		return chunks;
	}

	let show_preview = false;

	let images = [
		{
			full: '/img/pdp/pg1.jpg',
			thumb: '/img/pdp/pg1small.jpg',
			title: 'Front Black'
		},
		{ full: '/img/pdp/pg2.jpg', thumb: '/img/pdp/pg2small.jpg', title: 'Back Black' },
		{ full: '/img/pdp/pg3.jpg', thumb: '/img/pdp/pg3small.jpg', title: 'Back Azul' },
		{ full: '/img/pdp/pg4.jpg', thumb: '/img/pdp/pg4small.jpg', title: 'Front Azul' }
	];
	let selected_image = images[0];

	let colors = [
		{ name: 'Dark Gray', color: '#585d61' },
		{ name: 'Azul', color: '#96ccbe' }
	];
	let selected_color = colors[0];

	let qty = 1;
	$: if (qty < 1) qty = 1;

	let read_more = false;

	let popular_items = [
		{
			component: ProductCard,
			image: '/img/popularitems/back1.png',
			name: 'Kristina Dam Oak Table With White Marble Top',
			price: '799.55'
		},
		{
			component: ProductCard,
			image: '/img/popularitems/back2.png',
			name: 'Kristina Dam Oak Table With White Marble Top',
			price: '2195.00'
		},
		{
			component: ProductCard,
			image: '/img/popularitems/back3.png',
			name: 'Activate Facial Mask and Charcoal Soap',
			price: '129.55'
		},
		{
			component: ProductCard,
			image: '/img/popularitems/back4.png',
			name: 'Cocktail Table Walnut|YES',
			price: '629.99'
		}
	];

	function add_to_cart() {
		let count = +localStorage.getItem('cart');
		count += qty;
		localStorage.setItem('cart', count);
		window.dispatchEvent(new Event('product_changed'))
	}
</script>

<Breadcrumbs>
	<Breadcrumb href="/" name="OSF Theme" />
	<Breadcrumb name="Ruffle Front V-Neck Cardigan" />
</Breadcrumbs>

<h1 class="text-center"><span class="d-none d-sm-inline">Ruffle Front </span>V-Neck Cardigan</h1>

<div class="container-fuild px-4">
	<div class="row">
		<!-- main image + thumbnails -->
		<div class="col col-12 col-md-6 col-lg-auto">
			<div class="row">
				<!-- main image -->
				<div class="col col-12 col-lg-8">
					<div class="main-image mx-auto">
						<img src={selected_image.full} class="img-fluid" alt="product" />
						<i class="bi bi-arrows-fullscreen" on:click={() => (show_preview = true)} />
					</div>
				</div>

				<!-- thumbnails -->
				<div class="col col-12 col-lg-auto">
					<!-- on non extra-small screens, we display aligned vertically -->
					<div class="row d-none d-lg-block mx-auto">
						{#each images as image}
							<div class="col col-auto">
								<img
									src={image.thumb}
									alt={image.title}
									title={image.title}
									class="thumb"
									class:active={selected_image == image}
									on:click={() => (selected_image = image)}
								/>
							</div>
						{/each}
					</div>

					<!-- on smaller screens, we use a carousel with 3 images per slide -->
					<div id="thumb-carousel" class="carousel slide d-lg-none" data-bs-ride="">
						<div class="carousel-inner">
							<!-- split thumbnail list into chunks of 3 -->
							{#each chunk(images, 3) as images, i}
								<div class="carousel-item" class:active={i == 0}>
									<div class="row justify-content-center g-0">
										{#each images as image}
											<div class="col col-auto">
												<img
													src={image.thumb}
													alt={image.title}
													title={image.title}
													class="thumb"
													class:active={selected_image == image}
													on:click={() => (selected_image = image)}
												/>
											</div>
										{/each}
									</div>
								</div>
							{/each}
						</div>
						<div class="carousel-indicators">
							{#each Array(Math.ceil(images.length / 3)) as _, i}
								<button
									type="button"
									data-bs-target="#thumb-carousel"
									data-bs-slide-to={i}
									class:active={i == 0}
									aria-current={i == 0}
									aria-label="Page {i + 1}"
								/>
							{/each}
						</div>
					</div>
				</div>
			</div>
		</div>

		<!-- info -->
		<div class="col">
			<span class="first-price">$299.99</span>
			<div class="colorlist">
				<span class="dot" style:background-color={selected_color.color} />

				<select bind:value={selected_color}>
					{#each colors as color}
						<option value={color}>{color.name}</option>
					{/each}
				</select>
			</div>
			<div class="add ">
				<div class="amount">
					<button on:click={() => qty--}>-</button>
					<input type="number" name="amount" bind:value={qty} min="1" />
					<button on:click={() => qty++}>+</button>
				</div>
				<button on:click={add_to_cart} class="cart-btn">Add to cart</button>
			</div>
			<p>
				Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque
				laudantium, totam rem aperiam, eaque ipsa quae ab illo inventore Beatae vitae dicta sunt
				explicabo. <br />
				Nemo enim ipsam voluptatem
				<span id="dots" />
				<span class:d-none={!read_more}>
					quia voluptas sit aspernatur aut odit aut fugit, sed quia consequuntur magni dolores eos
					qui ratione voluptatem sequi nesciunt. Neque porro quisquam est, qui dolorem ipsum quia
					dolor sit amet, consectetur, adipisci velit, sed quia non numquam eius modi tempora
					incidunt ut labore et dolore magnam aliquam quaerat voluptatem. Ut enim ad minima veniam,
					quis nostrum exercitationem ullam corporis suscipit laboriosam, nisi ut aliquid ex ea
					commodi consequatur? Quis autem vel eum iure reprehenderit qui in ea voluptate velit esse
					quam nihil molestiae consequatur, vel illum qui dolorem eum fugiat quo voluptas nulla
					pariatur?
				</span>
			</p>
			<button class="read-more" on:click={() => (read_more = !read_more)}>
				Read {read_more ? 'Less' : 'More'}
			</button>

			<div class="share">
				Share
				<Social />
			</div>
		</div>
	</div>
</div>
<div class="infos  d-none d-lg-block ">
	<ul class="nav row justify-content-center" id="myTab" role="tablist">
		<li class="col col-auto nav-item " role="presentation">
			<button
				class="nav-link active"
				id="home-tab"
				data-bs-toggle="tab"
				data-bs-target="#home"
				type="button"
				role="tab"
				aria-controls="home"
				aria-selected="true">Description</button
			>
		</li>
		<li class="col col-auto nav-item" role="presentation">
			<button
				class="nav-link"
				id="profile-tab"
				data-bs-toggle="tab"
				data-bs-target="#profile"
				type="button"
				role="tab"
				aria-controls="profile"
				aria-selected="false">Additional Information</button
			>
		</li>
		<li class="col col-auto nav-item" role="presentation">
			<button
				class="nav-link"
				id="contact-tab"
				data-bs-toggle="tab"
				data-bs-target="#contact"
				type="button"
				role="tab"
				aria-controls="contact"
				aria-selected="false">Reviews (3)</button
			>
		</li>
	</ul>
</div>

<div class="tab-content d-none d-lg-block" id="myTabContent">
	<div class="tab-pane fade show active" id="home" role="tabpanel" aria-labelledby="home-tab">
		<div class="tab active row">
			<div class="column col-md-6 col1">
				<p>
					Aenean commodo ligula eget dolor. Aenean massa. Cum sociis natoque penatibus et magnis dis
					parturient montes, nascetur ridiculus mus.
				</p>
				<p>
					Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget
					dolor. Aenean massa.
				</p>
			</div>
			<div class="column col-md-6">
				<p>
					Cum sociis natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus.
					Donec quam felis, ultricies nec, pellentesque eu, pretium quis, sem. Nulla consequat massa
					quis enim. Donec pede justo, fringilla vel, aliquet nec, vulputate eget, arcu.
				</p>
			</div>
		</div>
	</div>
	<div class="tab-pane fade" id="profile" role="tabpanel" aria-labelledby="profile-tab">
		<div class="tab active row">
			<div class="column col-md-6 col1">
				<p>
					Aenean commodo ligula eget dolor. Aenean massa. Cum sociis natoque penatibus et magnis dis
					parturient montes, nascetur ridiculus mus.
				</p>
				<p>
					Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget
					dolor. Aenean massa.
				</p>
			</div>
			<div class="column col-md-6">
				<p>
					Cum sociis natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus.
					Donec quam felis, ultricies nec, pellentesque eu, pretium quis, sem. Nulla consequat massa
					quis enim. Donec pede justo, fringilla vel, aliquet nec, vulputate eget, arcu.
				</p>
			</div>
		</div>
	</div>
	<div class="tab-pane fade" id="contact" role="tabpanel" aria-labelledby="contact-tab">
		<div class="tab active row">
			<div class="column col-md-6 col1">
				<p>
					Aenean commodo ligula eget dolor. Aenean massa. Cum sociis natoque penatibus et magnis dis
					parturient montes, nascetur ridiculus mus.
				</p>
				<p>
					Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget
					dolor. Aenean massa.
				</p>
			</div>
			<div class="column col-md-6">
				<p>
					Cum sociis natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus.
					Donec quam felis, ultricies nec, pellentesque eu, pretium quis, sem. Nulla consequat massa
					quis enim. Donec pede justo, fringilla vel, aliquet nec, vulputate eget, arcu.
				</p>
			</div>
		</div>
	</div>
</div>
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

	<div class="scroll  d-sm-block d-md-none ">
		<button on:click={() => window.scrollTo(0, 0)}>Scroll to top</button>
	</div>
</section>

<Benefits />

<style>
	.container-fuild {
		background-color: #ffffff;
	}

	.main-image {
		position: relative;
		width: fit-content;
	}

	.main-image i {
		position: absolute;
		top: 10px;
		left: 10px;
		color: #84bc22;
		cursor: pointer;
	}

	.thumb {
		margin: 8px;
		border: 1px solid gray;
		border-radius: 2px;
		width: 72px;
		opacity: 0.5;
	}

	.thumb.active {
		border-color: #84bc22;
		opacity: 1;
	}

	.carousel-indicators {
		position: static;
	}
	.carousel-indicators button {
		border: 2px solid transparent;
		background-color: darkgray;
		border-radius: 50%;
		width: 10px;
		height: 10px;
	}

	.carousel-indicators button.active {
		border-color: black;
		background-color: white;
	}

	.first-price {
		font-size: 44px;
		font-weight: bold;
		color: #262a32;
		background-color: inherit;
	}
	.colorlist {
		border: 1px solid #7d7a77;
		width: fit-content;
		border-radius: 20px;
		padding: 2px 2px;
		background-color: white;
		overflow: hidden;
	}
	.dot {
		border-radius: 50%;
		height: 15px;
		width: 15px;
		display: inline-block;
		margin-left: 5px;
		margin-top: 5px;
	}
	.colorlist select {
		border: none;
		background-color: inherit;
	}
	.amount {
		background-color: #ffffff;
		color: #262a32;
		margin: 10px 0px;
		cursor: pointer;
		width: fit-content;
		border-radius: 25px;
		padding: 5px 5px;
		border: 1px solid #7d7a77;
		overflow: hidden;
	}
	.amount input {
		border: none;
		color: #262a32;
		cursor: pointer;
		background-color: #ffffff;
	}

	.amount input::-webkit-outer-spin-button, /*hide the tml nr input */
	.amount input::-webkit-inner-spin-button {		
		-webkit-appearance: none;
		margin: 0;
	}

	.amount input[type='number'] {
		-moz-appearance: textfield; /* Firefox */
	}

	.amount button {
		border: none;
		background-color: #ffffff;
	}

	.cart-btn {
		color: #ffffff;

		cursor: pointer;
		border-radius: 25px;
		background-color: #84bc22;
		padding-top: 5px;
		padding-bottom: 5px;
		padding-left: 20px;
		padding-right: 20px;
		text-transform: uppercase;
		width: fit-content;
	}
	p {
		font-size: 16px;
		font-family: Lato, sans-serif;
	}

	.read-more {
		border: none;
		background-color: inherit;
		padding-top: 10px;
		padding-bottom: 30px;
		color: #84bc22;

		font-size: 18px;
	}
	/* nu-tabs */
	.infos {
		background-color: #ffffff;
		padding-top: 80px;
	}
	#myTab button {
		border: none;
		border-radius: 32px 32px 0px 0px;
		background-color: #ffffff;
		text-decoration: none;
		color: #262a32;
		font-size: 24px;
		cursor: pointer;
		transition: all 0.2s ease;
		padding: 24px 48px;
	}
	#myTab button:hover,
	#myTab button.active {
		background-color: #262a32;
		color: #ffffff;
	}
	#myTabContent {
		color: #ffffff;
		background-color: #262a32;
		font-size: 18px;
		line-height: 1.5;
		padding: 60px 50px;
		margin-bottom: 40px;
	}
	/*popular items */
	.popular-items {
		max-width: 100%;

		padding-bottom: 50px;
	}
	.popular-items h4 {
		color: black;
		text-align: center;
		font-family: Lato ExtraBold, sans-serif;
		font: size 20px;
		padding-top: 2px;
		width: fit-content;
		margin-top: -18px;
	}

	.price {
		color: #84bc22;
		background-color: #ffffff;
		border-radius: 16px;
	}

	.popular-items .hr {
		border-top: 2px solid #3c4047;
	}
	.divider {
		margin: 0 2.5%;
		padding-top: 40px;
	}
	.scroll a {
		text-decoration: none;
		color: #ffffff;
	}
	.scroll {
		width: fit-content;
		margin-left: 36%;
		margin-right: 37%;
		margin-top: 8%;
		background-color: #84bc22;
		cursor: pointer;
		border-radius: 25px;
		border: 1px solid #84bc22;
		text-transform: uppercase;
		padding-top: 5px;
		padding-bottom: 5px;
		padding-left: 20px;
		padding-right: 20px;
	}
</style>
