<script>
	export let slide = true;
	export let items = [];
</script>

<div class="container-fluid px-4">
	<!-- on large screens, show list of all products -->
	<div class="row justify-content-center g-5 {slide ? 'd-none d-sm-flex' : ''}">
		{#each items as item}
			<div class="col-auto">
				<svelte:component this={item.component} {...item} />
			</div>
		{/each}
	</div>

	{#if slide}
		<!-- on smaller screens, we use a carousel with 1 product images per slide -->
		<div id="popular-carousel" class="carousel slide d-sm-none" data-bs-ride="">
			<div class="carousel-inner">
				<!-- split thumbnail list into chunks of 3 -->
				{#each items as item, i}
					<div class="carousel-item" class:active={i == 0}>
						<div class="row justify-content-center g-0">
							<svelte:component this={item.component} {...item} />
						</div>
					</div>
				{/each}
			</div>

			<div class="carousel-indicators">
				{#each items as { name }, i}
					<button
						type="button"
						data-bs-target="#popular-carousel"
						data-bs-slide-to={i}
						class:active={i == 0}
						aria-current={i == 0}
						aria-label={name}
					/>
				{/each}
			</div>
		</div>
	{/if}
</div>

<style>
	.carousel-indicators {
		position: static;
		margin-top: 10px;
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
</style>
