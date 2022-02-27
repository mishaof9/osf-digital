<script>
	import ProductCard from '$lib/cards/ProductCard.svelte';
	import FeaturedProduct from '$lib/FeaturedProduct.svelte';
</script>

<section class="category-page">
	<div class="wrapper home-category">
		<ul>
			<li class="li-hm"><a href="/">Home </a></li>
			<li class="li-slash">/</li>
			<li class="li-category"><a href="/"> Category Landing Services</a></li>
		</ul>
		<h2>Services</h2>
	</div>

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
<!--
<CardContainer>
	<ProductCard
		name="Kristina Dam Oak Table With White Marble Top"
		img="static/img/popularitems/item3.png"
		price="799.55"
	/>
	<ProductCard
		name="EAMES x Cast + Crew - Custom Powder Coated "
		img="static/img/popularitems/item1.png"
		price="799.55"
	/>
	<ProductCard
		name="Activate Facial Mask and Charcoal Soap"
		img="static/img/popularitems/item2.png"
		price="129.55"
	/>
	<ProductCard
		name="Vitra Cork Stool B, Cork - Design Within Reach"
		img="static/img/popularitems/item12.png"
		price="299.99"
	/>
	<ProductCard
		name="Hay-About A Lounge Chair AAL 93"
		img="static/img/popularitems/item6.png"
		price="659.55"
	/>
	<ProductCard name="TORY DESK CALENDAR" img="static/img/popularitems/item5.png" price="410.99" />
	<ProductCard
		name="CH445 Wing Chair on  SUITE NY"
		img="static/img/popularitems/notfound.png"
		price="330.55"
	/>
	<ProductCard
		name="CH445 Wing Chair on  SUITE NY"
		img="static/img/popularitems/notfound.png"
		price="330.55"
	/>
	<ProductCard
		name="Kristina Dam Oak Table With White Marble Top"
		img="static/img/popularitems/notfound.png"
		price="2195.00"
	/>
	<ProductCard
		name="MONOQI | Ø55 Crossit  Table - Wht/Grn"
		img="static/img/popularitems/notfound.png"
		price="299.99"
	/>
	<ProductCard
		name="Vitra Cork Stool B, Cork - Design Within Reach"
		img="static/img/popularitems/item6.png"
		price="870.95"
	/>
	<ProductCard
		name="Activate Facial Mask and Charcoal Soap "
		img="static/img/popularitems/notfound.png"
		price="199.55"
	/>
	<ProductCard
		name="Hay-About A Lounge Chair AAL 93"
		img="static/img/popularitems/notfound.png"
		price="659.55"
	/>
	<ProductCard name="TORY DESK CALENDAR" img="static/img/popularitems/item7.png" price="410.99" />
	<ProductCard
		name="EAMES x Cast + Crew - Custom Powder Coated "
		img="static/img/popularitems/menu.jpg"
		price="330.55"
	/>
	<ProductCard
		name="CH445 Wing Chair on  SUITE NY"
		img="static/img/popularitems/notfound.png"
		price="330.55"
	/>
</CardContainer>
-->
<div class="button load-more"> Load more</div>
	

<FeaturedProduct />

<style>
	.home-category ul {
		display: flex;
		list-style: none;
		justify-content: center;
		margin-top: 60px;
	}
	.home-category ul li {
		padding: 0px 5px;
	}
	.li-hm a {
		text-decoration: none;
		font-size: 17px;
		color: #84bc22;
		font-weight: bold;
	}
	.li-category a {
		text-decoration: none;
		font-size: 17px;
		color: black;
	}
	.home-category h2 {
		font-weight: bold;
		font-size: 40px;
		padding-top: 10px;
		text-align: center;
	}
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
		width:fit-content;
		margin:5% auto;
	    text-align: center;
	
		
		
	}
</style>
