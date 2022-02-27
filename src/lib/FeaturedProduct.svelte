<script>
	import Card from '$lib/cards/Card.svelte';
</script>

<section class="featured-product wrapper d-none d-lg-block p-4">
	<div>
		<h3>Featured Product</h3>
		<h6>Unde omnis iste natus error sit voluptatem</h6>
	</div>
	<div
		id="featured-carousel"
		class="carousel slide"
		data-bs-ride="carousel"
		data-bs-interval="5000"
	>
		<div class="row slider">
			<button
				type="button"
				class="featured-slider-control"
				data-bs-target="#featured-carousel"
				data-bs-slide="prev">&lt;</button
			>
			<div class="hr" />
			///
			<div class="hr" />
			<button
				type="button"
				class="featured-slider-control"
				data-bs-target="#featured-carousel"
				data-bs-slide="next">&gt;</button
			>
		</div>
		<div class="carousel-inner">
			<div class="carousel-item active">
				<div class="row g-0">
					<div class="col">
						<Card>
							<div class="featured">
								<img src="static/img/cards/calendar.png" />
								<p>Kristina Dam Oak Table With White Marble</p>
								<h5>Awesome</h5>
							</div>
						</Card>
					</div>
					<div class="col">
						<Card>
							<div class="featured">
								<img src="static/img/cards/gracioushome.png" />
								<p class="card-text">Kristina Dam Oak Table With White Marble</p>
								<h5>Marketing</h5>
							</div>
						</Card>
					</div>
					<div class="col">
						<Card>
							<div class="featured">
								<img src="static/img/cards/pen.png" />
								<p>Kristina Dam Oak Table With White Marble</p>
								<h5>Awesome</h5>
							</div>
						</Card>
					</div>
					<div class="col">
						<Card>
							<div class="featured">
								<img src="static/img/cards/salesforce.png" />
								<p>Kristina Dam Oak Table With White Marble</p>
								<h5>Marketing</h5>
							</div>
						</Card>
					</div>
				</div>
			</div>
			<div class="carousel-item">
				<div class="row">
					<div class="col">
						<Card>
							<div class="featured">
								<img src="static/img/cards/salesforce.png" alt="salesforce" />
								<p>Kristina Dam Oak Table With White Marble</p>
								<h5>Awesome</h5>
							</div>
						</Card>
					</div>
					<div class="col">
						<Card>
							<div class="featured">
								<img src="static/img/cards/pen.png" alt="pen" />
								<p class="card-text">Kristina Dam Oak Table With White Marble</p>
								<h5>Marketing</h5>
							</div>
						</Card>
					</div>
					<div class="col">
						<Card>
							<div class="featured">
								<img src="static/img/cards/gracioushome.png" alt="gracioushome" />
								<p>Kristina Dam Oak Table With White Marble</p>
								<h5>Awesome</h5>
							</div>
						</Card>
					</div>
					<div class="col">
						<Card>
							<div class="featured">
								<img src="static/img/cards/calendar.png" alt="calendar" />
								<p>Kristina Dam Oak Table With White Marble</p>
								<h5>Marketing</h5>
							</div>
						</Card>
					</div>
				</div>
			</div>
		</div>
	</div>
</section>

<style>
	/*featured product */

	.featured-product {
		background-color: #262a32;
		max-width: 100%;
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

	.featured-slider-control {
		border: none;
		width: 30px;
		height: 30px;
		color: rgb(253, 253, 253);
		background-color: #2d343a;
		margin-top: -5px;
	}

	.featured {
		height: 295px;
	}

	.featured p {
		text-align: center;
		font-size: 20px;
		margin-top: 10px;
	}
	.featured h5 {
		color: #84bc22;
		text-align: center;
		font-family: Lato ExtraBold, sans-serif;
		font-size: 18px;
	}
</style>
