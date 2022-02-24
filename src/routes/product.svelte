<script>
	import Benefits from '$lib/Benefits.svelte';
	import CardRow from '$lib/CardRow.svelte';
	import ProductCard from '$lib/ProductCard.svelte';
</script>

<!--product detailed page-->
<section class="product-page">
	<div class="wrapper home-product">
		<ul>
			<li class="li-hm"><a href="/">Home</a></li>
			<li class="li-slash">/</li>
			<li class="li-osf-theme"><a href="/">OSF Theme</a></li>
			<li class="li-slash">/</li>
			<li class="li-description">Ruffle Front V-Neck Cardigan</li>
		</ul>
		<h2>Ruffle Front V-Neck Cardigan</h2>
	</div>
	<div class=" row main-product">
		<div class=" pictures column col-4">
			<img src="static/img/pdp/pg1.jpg" alt="first picture" class="main-picture" />
		</div>
		<div class="small-pictures column col-4">
			<img src="static/img/pdp/pg1small.jpg" alt="first picture2" />
			<img src="static/img/pdp/pg2small.jpg" alt="second picture" />
			<img src="static/img/pdp/pg3small.jpg" alt="third picture" />
			<img src="static/img/pdp/pg4small.jpg" alt="fourth picture" />
		</div>

		<div class="about column  col-4">
			<span class="price">$299.99</span>
			<div class="colorlist">
				<span class="dot" />

				<select name="colorlist">
					<option value="Dark Gray">Dark Gray</option>
					<option value="Aqua">Aqua</option>
				</select>
			</div>
			<div class="add row">
				<div class="amount column col-6">
					<button class="minus">-</button>
					<input type="number" name="amount" />
					<button class="plus">+</button>
				</div>
				<button class="cart-btn column col-6">Add to cart</button>
			</div>
			<p>
				Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque
				laudantium, totam rem aperiam, eaque ipsa quae ab illo inventore Beatae vitae dicta sunt
				explicabo. <br />
				Nemo enim ipsam voluptatem <span id="dots" /><span id="more"
					>quia voluptas sit aspernatur aut odit aut fugit, sed quia consequuntur magni dolores eos
					qui ratione voluptatem sequi nesciunt. Neque porro quisquam est, qui dolorem ipsum quia
					dolor sit amet, consectetur, adipisci velit, sed quia non numquam eius modi tempora
					incidunt ut labore et dolore magnam aliquam quaerat voluptatem. Ut enim ad minima veniam,
					quis nostrum exercitationem ullam corporis suscipit laboriosam, nisi ut aliquid ex ea
					commodi consequatur? Quis autem vel eum iure reprehenderit qui in ea voluptate velit esse
					quam nihil molestiae consequatur, vel illum qui dolorem eum fugiat quo voluptas nulla
					pariatur?
				</span>
			</p>
			<button onclick="myFunction()" id="myBtn"> Read more</button>

			<div class="share column">
				<span>Share</span>
				<ul>
					<a href="https://www.facebook.com/OSFGlobalServices/" target="_blank">
						<i class="bi bi-facebook" />
					</a>
					<a href="https://www.google.com" target="_blank">
						<i class="bi bi-google" />
					</a>
					<a href="https://twitter.com/osfglobal" target="_blank">
						<i class="bi bi-twitter" />
					</a>
					<a href="https://www.pinterest.ca/osfglobal/" target="_blank">
						<i class="bi bi-pinterest" />
					</a>
				</ul>
			</div>
		</div>
	</div>

	<div class="tabs-info">
		<ul>
			<li class="active">Description</li>
			<li>Additional information</li>
			<li>Reviews (3)</li>
		</ul>
		<div class="tab-container">
			<div class="tab active row">
				<div class="column col-md-6 col1">
					<p>
						Aenean commodo ligula eget dolor. Aenean massa. Cum sociis natoque penatibus et magnis
						dis parturient montes, nascetur ridiculus mus.
					</p>
					<p>
						Lorem ipsum dolor sit amet, consectetuer adipiscing elit. Aenean commodo ligula eget
						dolor. Aenean massa.
					</p>
				</div>
				<div class="column col-md-6">
					<p>
						Cum sociis natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus.
						Donec quam felis, ultricies nec, pellentesque eu, pretium quis, sem. Nulla consequat
						massa quis enim. Donec pede justo, fringilla vel, aliquet nec, vulputate eget, arcu.
					</p>
				</div>
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
	<CardRow>
		<ProductCard
			name="Kristina Dam Oak Table With White Marble Top"
			img="static/img/popularitems/back1.png"
			price="799.55"
		/>
		<ProductCard
			name="Kristina Dam Oak Table With White Marble Top"
			img="static/img/popularitems/back2.png"
			price="2195.00"
		/>
		<ProductCard
			name="Activate Facial Mask and Charcoal Soap"
			img="static/img/popularitems/back3.png"
			price="129.55"
		/>
		<ProductCard
			name="Cocktail Table Walnut|YES  "
			img="static/img/popularitems/back4.png"
			price="629.99"
		/>
	</CardRow>
</section>

<Benefits />

<style>
	/*product page*/

	.card2 {
		margin-top: -115px;
	}
	.product-page {
		margin-top: 30px;
		margin-bottom: 100px;
		padding-bottom: 70px;
	}

	.home-product h2 {
		font-weight: bold;
		font-size: 44px;
		padding-left: 50px;
		padding-top: 20px;
		text-align: center;
	}
	.home-product ul {
		display: flex;
		list-style: none;
		justify-content: center;
	}
	.li-hm a {
		text-decoration: none;
		font-size: 17px;
		color: #84bc22;
		font-weight: bold;
	}
	.li-osf-theme a {
		text-decoration: none;
		font-size: 17px;
		color: #84bc22;
		font-weight: bold;
	}
	.li-slash {
		padding-left: 5px;
		padding-right: 5px;
	}
	.main-product {
		margin-top: 40px;
		background-color: #ffffff;
	}
	.main-picture {
		margin-right: 45px;
		height: 450px;
	}
	.pictures {
		width: 30%;
		margin-right: 70px;
		margin-left: 10px;
		margin-top: 20px;
	}
	.small-pictures {
		width: 90px;
		margin-top: 20px;
		margin-left: 20px;
		padding: 0;
	}
	.about {
		margin-left: 150px;
		margin-top: 20px;
	}
	.about .price {
		font-size: 44px;
		font-weight: bold;
		color: #262a32;
		background-color: inherit;
	}
	.about .colorlist {
		border: 1px solid #7d7a77;
		width: fit-content;
		border-radius: 20px;
		padding: 2px 2px;
		background-color: white;
	}
	.dot {
		background-color: #2d343a;
		border-radius: 50%;
		height: 15px;
		width: 15px;
		display: inline-block;
		margin-left: 5px;
		margin-top: 5px;
	}
	.about select {
		border: none;
		background-color: #ffffff;
		width: 165px;
	}
	.amount {
		background-color: #ffffff;
		color: #262a32;
		margin: 10px 10px;
		cursor: pointer;
		width: fit-content;
		border-radius: 25px;
		padding-top: 5px;
		border: 1px solid #7d7a77;
	}
	.amount input {
		border: none;
		color: #262a32;
		cursor: pointer;
		width: 50px;
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

	.amount .minus {
		border: none;
		background-color: #ffffff;
	}
	.amount .plus {
		border: none;
		background-color: #ffffff;
	}
	.share span {
		float: left;
		margin-right: 30px;
		color: #7d7a77;
	}
	.share a {
		padding-right: 30px;
		text-decoration: none;
	}
	.share ul {
		list-style: none;
	}
	.share ul a i {
		color: #7d7a77;
	}
	.about p {
		font-size: 16px;
	}
	.cart-btn {
		color: #ffffff;
		margin: 10px 10px;
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
	#myBtn {
		border: none;
		background-color: inherit;
		padding-top: 10px;
		padding-bottom: 30px;
		color: #84bc22;
		margin-right: 250px;
		font-size: 18px;
	}

	/*product page tab info */
	.tabs-info {
		margin-top: 80px;
	}
	.tabs-info ul {
		display: flex;
		list-style: none;
		justify-content: center;
		margin-bottom: 0px;
	}
	.tabs-info > ul {
		text-align: center;
	}
	.tabs-info > ul li {
		display: inline-block;
		margin: 0px 16px;
		padding: 24px 48px;
		font-size: 24px;
		border-radius: 32px 32px 0px 0px;
		color: #bdc3c7;
		background-color: inherit;
		cursor: pointer;
		transition: all 0.2s ease;
	}
	.tabs-info > ul li:hover {
		color: #ffffff;
		background-color: #262a32;
	}
	.tabs-info > ul li.active {
		color: #ffffff;
		background-color: #262a32;
	}
	.tabs-info .tab-container .tab {
		display: flex;

		flex-wrap: wrap;
		align-items: flex-start;
		color: #ffffff;
		background-color: #262a32;
		padding-top: 70px;
		padding-bottom: 30px;
		overflow: hidden;
		position: absolute;
		left: 0;
		top: 0;
		right: 0;
		bottom: 0;
		opacity: 0;
		visibility: hidden;
		transition: all 0.6s ease;
	}
	.tabs-info .tab-container .column p {
		color: #ffffff;
		margin-bottom: 30px;

		font-size: 18px;
		line-height: 1.5;
	}
	.tabs-info .tab-container .col1 {
		float: left;
	}
	.tabs-info .tab-container .tab.active {
		visibility: visible;
		opacity: 1;
		float: left;
		position: relative;
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
	.popular-items .card-text {
		text-align: center;
		font-size: 15px;
		color: black;
		padding-top: 130px;
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
		border-radius: 16px;
	}

	.popular-items .hr {
		border-top: 2px solid #3c4047;
		width: 400px;
	}
	.divider {
		padding: 60px 53px 50px 53px;
		align-self: center;
		margin-left: 60px;
	}
</style>
