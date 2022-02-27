<script>
	import { createEventDispatcher } from 'svelte';
	import Modal from '$lib/modals/Modal.svelte';

	const dispatch = createEventDispatcher();
	const close = () => dispatch('close');

	function accept() {
		close();
	}
</script>

<Modal on:close>
	<div class="cookies">
		<h6>This website uses cookies</h6>
		<p>
			OSF uses its own and third-party cookies for statistical purposes, to know your preferences,
			for website performance <br /> and interaction with social media offering publicity tailored
			to your interests. If you continue browsing, we consider that you accept its use.<br />
			You can expand this information consulting our <a href="#">Cookies Policy Page</a>.
			<span id="close-cookies"><i class="fas fa-times" /></span>
		</p>
		<button class="accept-cookies btn" on:click={accept}>Accept</button>
	</div>
</Modal>

<style>
	.cookies {
		position: absolute;
		width: 1160px;
		height: 140px;
		text-align: left;
		border-radius: 10px;
		padding: 10px;
		background-color: white;
		margin-top: 400px;
		margin-left: 60px;
	}
	.cookies h6 {
		color: #84bc22;
		font-family: Lato, sans-serif;
		font-size: 16px;
		font-weight: bold;
	}
	.cookies p {
		font-family: Lato, sans-serif;
		font-size: 14px;
		line-height: 2;
	}
	.cookies a {
		color: #84bc22;
		text-decoration: none;
	}
	.accept-cookies {
		color: #ffffff;
		background-color: #84bc22;
		border-radius: 16px;
		padding: 2px 20px;
		text-transform: uppercase;
		position: absolute;
		right: 20px;
		bottom: 20px;
	}
</style>
