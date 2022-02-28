<script>
	import { createEventDispatcher } from 'svelte';

	const dispatch = createEventDispatcher();
	const close = () => dispatch('close');

	function handle_keydown(event) {
		if (event.key == 'Escape') close();
	}
</script>

<svelte:window on:keydown={handle_keydown} />

<div on:click|self={close}>
	<slot />
</div>

<style>
	div {
		position: fixed;
		top: 0;
		left: 0;
		width: 100vw;
		height: 100vh;
		background-color: rgba(100, 100, 100, 0.5);
		z-index: 1000;

		display: flex;
		justify-content: center;
		align-items: center;
	}
</style>
