<script>
	export let show = false;
	export let src;
	export let alt;
</script>

{#if show}
	<img {src} {alt} />
{/if}
