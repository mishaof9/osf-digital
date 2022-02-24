<script>
	import Card from '$lib/Card.svelte';

	export let img;
	export let name;
	export let price;
	export let discounted = false;
</script>

<Card>
	<img src={img} alt={name} />
	<p class="name">{name}</p>
	{#if discounted}
		<div class="btn-group discounted">
			<button type="button" class="btn discount-price">$ {price}</button>
			<button type="button" class="btn buynow">BUY NOW</button>
		</div>
	{:else}
		<p class="price">$ {price}</p>
	{/if}

	<div class="overlay">
		<i class="bi bi-plus" />
		<i class="bi bi-heart-fill" />
	</div>
</Card>

<style>
	img {
		height: 260px;
		margin-bottom: 15px;
	}

	.name {
		height: 30px;
		margin: 5px 20px;
	}
	.price {
		margin-top: 20px;
	}

	.discounted {
		border: 2px solid #e5e5e5;
		border-radius: 16px;
	}

	.discount-price {
		color: #84bc22;
		border-right: 1px solid #e5e5e5;
	}

	.buynow {
		font-weight: bold;
	}

	.overlay {        
		display: flex;
		align-items: center;
		justify-content: center;

		position: absolute;
		top: 0;
		height: 100%;
		width: 100%;
		opacity: 0;
		transition: 0.1s linear;
		background-color: rgba(53, 202, 126, 0.8);

	}

	.overlay:hover {
		opacity: 1;
	}

	.overlay i {
		display: inline-block;
		width: 90px;
		height: 90px;
		line-height: 90px;
		text-align: center;
		border-radius: 50%;
		background-color: white;
		margin: 5px;
        cursor: pointer;
	}

	.overlay .bi-plus {
		color: #23c46e;
		font-size: 60px;
	}
	.overlay .bi-heart-fill {
		color: #e73c68;
		font-size: 30px;
	}
</style>
