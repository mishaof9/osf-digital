<script>
	import Card from '$lib/cards/Card.svelte';
</script>

<Card>
	<img src="/static/img/popularitems/item13.jpg" />
	<div>
		<p>My dragons are misbehaving again.</p>
        <p>Unbelieveable!</p>
		<p><i class="bi bi-chat-dots" />5H AGO</p>
    </div>
</Card>

<style>
	div {
		display: flex;
		position: absolute;
		top: 0;
		height: 100%;
		width: 100%;

		padding: 20px;

		flex-direction: column;
		align-items: start;
		justify-content: end;
		text-align: left;

		background: rgb(106, 93, 143);
		background: linear-gradient(0deg, rgba(106, 93, 143, 0.8) 0%, rgba(203, 100, 138, 0.8) 100%);
		color: #fff;

		}

		i {
			margin-right: 10px;
			color: #84bc22;
		}
</style>
