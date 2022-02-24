<script>
	import Card from '$lib/Card.svelte';
</script>

<Card>
	<img src="static/img/popularitems/item13.jpg" />
	<div class="content">
		<p>My dragons are misbehaving again.</p>
        <p>Unbelieveable!</p>
		<p>5H AGO</p>
    </div>
	<div class="overlay" />
</Card>

<style>
	.content {
		position: absolute;
		top: 200px;
		text-align: center;
		color: #ffffff;
        padding-left:5px;
	}

	.overlay {
		position: absolute;
		top: 0;
		height: 100%;
		width: 100%;
		opacity: 0;
		transition: 0.1s linear;
		background: rgb(106, 93, 143);
		background: linear-gradient(0deg, rgba(106, 93, 143, 0.8) 0%, rgba(203, 100, 138, 0.8) 100%);
	}

	.overlay:hover {
		opacity: 1;
	}
</style>
