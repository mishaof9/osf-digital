<script>
	import ProductCard from '$lib/cards/ProductCard.svelte';
	import FeaturedProduct from '$lib/FeaturedProduct.svelte';
import Breadcrumb from '$lib/nav/Breadcrumb.svelte';
import Breadcrumbs from '$lib/nav/Breadcrumbs.svelte';
	import PopularItems from '$lib/Products.svelte';

	let products = [
		{
			component: ProductCard,
			image: '/img/popularitems/item3.png',
			name: 'Kristina Dam Oak Table With White Marble Top',
			price: '799.55'
		},
		{
			component: ProductCard,
			image: '/img/popularitems/item1.png',
			name: 'EAMES x Cast + Crew - Custom Powder Coated ',
			price: '799.55'
		},
		{
			component: ProductCard,
			image: '/img/popularitems/item2.png',
			name: 'Activate Facial Mask and Charcoal Soap',
			price: '129.55'
		},
		{
			component: ProductCard,
			image: '/img/popularitems/item12.png',
			name: 'Vitra Cork Stool B, Cork - Design Within Reach',
			price: '299.99'
		},
		{
			component: ProductCard,
			image: '/img/popularitems/item6.png',
			name: 'Hay-About A Lounge Chair AAL 93',
			price: '659.55'
		},
		{
			component: ProductCard,
			image: '/img/popularitems/item5.png',
			name: 'TORY DESK CALENDAR',
			price: '410.99'
		},

		{
			component: ProductCard,
			image: '/img/popularitems/notfound.png',
			name: 'CH445 Wing Chair on  SUITE NY',
			price: '330.55'
		},
		{
			component: ProductCard,
			image: '/img/popularitems/notfound.png',
			name: 'CH445 Wing Chair on  SUITE NY',
			price: '330.55'
		},
		{
			component: ProductCard,
			image: '/img/popularitems/notfound.png',
			name: 'Kristina Dam Oak Table With White Marble Top',
			price: '2195.00'
		},
		{
			component: ProductCard,
			image: '/img/popularitems/notfound.png',
			name: 'MONOQI | Ø55 Crossit  Table - Wht/Grn',
			price: '299.99'
		},
		{
			component: ProductCard,
			image: '/img/popularitems/item6.png',
			name: 'Vitra Cork Stool B, Cork - Design Within Reach',
			price: '870.95'
		},
		{
			component: ProductCard,
			image: '/img/popularitems/notfound.png',
			name: 'Activate Facial Mask and Charcoal Soap ',
			price: '199.55'
		},
		{
			component: ProductCard,
			image: '/img/popularitems/notfound.png',
			name: 'Hay-About A Lounge Chair AAL 93',
			price: '659.55'
		},
		{
			component: ProductCard,
			image: '/img/popularitems/item7.png',
			name: 'TORY DESK CALENDAR',
			price: '410.99'
		},

		{
			component: ProductCard,
			image: '/img/popularitems/menu.jpg',
			name: 'EAMES x Cast + Crew - Custom Powder Coated ',
			price: '330.55'
		},
		{
			component: ProductCard,
			image: '/img/popularitems/notfound.png',
			name: 'CH445 Wing Chair on  SUITE NY',
			price: '330.55'
		}
	];
</script>

<Breadcrumbs>
	<Breadcrumb href="/" name="OSF Theme" />
	<Breadcrumb name="Category Landing Services" />
</Breadcrumbs>

<h1 class="text-center">Services</h1>

<section class="category-page">
	<div class="filters">
		<div class="row row-cols-1 row-cols-md-2 row-cols-xl-3">
			<div class="col price-filter">
				<label for="price">Price</label>
				<select name="price" id="price">
					<option value="">$0.00-$100.00</option>
					<option value="">$100.00-$300.00</option>
					<option value="">$300.00-$500.00</option>
					<option value="">$500.00-$1000.00</option>
				</select>
			</div>
			<div class="col brands-filter ">
				<label for="brands"> Brands </label>
				<select name="brands" id="brands">
					<option value="">Ukraine Sport</option>
					<option value="">United Kingdom Sport</option>
					<option value="">Japanese Sport</option>
				</select>
			</div>
			<div class="col size-filter">
				<label for="size"> Size </label>
				<select name="size" id="size">
					<option value="">Small</option>
					<option value="">Medium</option>
					<option value="">Large</option>
				</select>
			</div>
			<div class="col color-filter">
				<label for="color">Color</label>
				<input type="radio" name="color" class="select-color color-white" />
				<input type="radio" name="color" class="select-color color-azul" />
				<input type="radio" name="color" class="select-color color-black" />
				<input type="radio" name="color" class="select-color color-green" />
				<input type="radio" name="color" class="select-color color-blue" />
				<input type="radio" name="color" class="select-color color-orange" />
				<input type="radio" name="color" class="select-color color-red" />
				<input type="radio" name="color" class="select-color color-beige" />
			</div>

			<div class="col sort-filter ">
				<label for="sort"> Sort </label>
				<select name="sort" id="sort">
					<option value="">Price</option>
					<option value="">Brands</option>
					<option value="">Size</option>
				</select>
			</div>

			<div class="col show-filter ">
				<label for="show"> Show </label>
				<select name="show" id="show">
					<option value="">16 per page</option>
					<option value="">48 per page</option>
					<option value="">96 per page</option>
				</select>
			</div>
		</div>
	</div>

	<div class="total-results"><h6>12.932 results in apparel</h6></div>
</section>

<PopularItems slide={false} items={products} />

<div class="button load-more">Load more</div>

<FeaturedProduct />

<style>
	.filters {
		background-color: #fff;
		margin: 0px 4.3%;
		padding-left: 2.5%;
		padding-right: 2.5%;
		padding-bottom: 30px;
	}

	.filters select {
		border-radius: 16px;
		color: black;
		background-color: #ffffff;
		padding: 2px 20px;
		margin-top: 35px;
		width: 200px;
		text-align: center;
		border: 1px solid lightgray;
	}

	.filters label {
		width: 50px;
		height: 25px;
	}

	.filters .color-filter {
		margin-top: 35px;
	}
	.filters .color-filter input[type='radio'] {
		margin-right: 5px;
	}
	.filters .color-filter label {
		margin-right: -15px;
		padding-right: 0px;
	}
	/* color filter input*/
	.select-color {
		appearance: none;
		width: 20px;
		height: 20px;
		border: 3px solid black;
		border-radius: 50%;
	}

	.select-color:before {
		content: '';
		display: block;
		width: 120%;
		height: 120%;
		margin: -1px 0px 0px -1px;
		border-radius: 50%;
	}
	.select-color.color-white {
		border-color: #ffffff;
	}
	.select-color.color-white:checked:before {
		background: #ffffff;
	}
	.select-color.color-azul {
		border-color: #43c0cf;
	}
	.select-color.color-azul:checked:before {
		background-color: #43c0cf;
	}
	.select-color.color-black {
		border-color: #3d402f;
	}
	.select-color.color-black:checked:before {
		background-color: #3d402f;
	}
	.select-color.color-green {
		border-color: #84bc22;
	}
	.select-color.color-green:checked:before {
		background-color: #84bc22;
	}
	.select-color.color-blue {
		border-color: #315bbd;
	}
	.select-color.color-blue:checked:before {
		background-color: #315bbd;
	}
	.select-color.color-orange {
		border-color: #ec6115;
	}
	.select-color.color-orange:checked:before {
		background-color: #ec6115;
	}
	.select-color.color-red {
		border-color: #dc041d;
	}
	.select-color.color-red:checked:before {
		background-color: #dc041d;
	}
	.select-color.color-beige {
		border-color: #efead7;
	}
	.select-color.color-beige:checked:before {
		background-color: #efead7;
	}
	.total-results {
		text-align: center;
		font-family: Lato, sans-serif;
		font-size: 16px;
	}
	.load-more {
		border-radius: 16px;
		border: 1px solid lightgray;
		color: #ffffff;
		background-color: #84bc22;
		padding: 5px 20px;
		width: fit-content;
		margin: 5% auto;
		text-align: center;
	}
</style>
