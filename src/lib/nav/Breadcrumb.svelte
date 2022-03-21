<script>
	export let href = '';
	export let name;

	let active = href == '';
</script>

{#if active}
	<li class="breadcrumb-item active" aria-current="page">
		{name}
	</li>
{:else}
	<li class="breadcrumb-item">
		<a {href}>{name}</a>
	</li>
{/if}

<style>
	a {
		text-decoration: none;
		font-size: 17px;
		color: #84bc22;
		font-weight: bold;
		padding: 0 10px;
		font-family: 'Times New Roman', Times, serif;
	}
</style>
