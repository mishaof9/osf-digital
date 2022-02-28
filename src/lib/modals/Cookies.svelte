<script>
	import { onMount } from 'svelte';
	import Modal from '$lib/modals/Modal.svelte';

	let show = false;
	const close = function() { show = false };
	
	function accept() {
		localStorage.setItem('accepted_cookies', true);
		close();
	}

	onMount(function() {
		const accepted = localStorage.getItem('accepted_cookies');
		if (!accepted) {
			setTimeout(function() { show = true }, 10000);
		}
	});
</script>

{#if show}
	<Modal on:close={close}>
		<div class="cookies">
			<div class="header">
				<h6>This website uses cookies</h6>
				<i on:click={close} class="bi bi-x-lg"/>
			</div>
			<p>
				OSF uses its own and third-party cookies for statistical purposes, to know your preferences,
				for website performance <br /> and interaction with social media offering publicity tailored
				to your interests. If you continue browsing, we consider that you accept its use.<br />
				You can expand this information consulting our <a href="#">Cookies Policy Page</a>.
			</p>
			<button class="accept" on:click={accept}>Accept</button>
		</div>
	</Modal>
{/if}

<style>
	.cookies {
		width: 95%;
		max-width: 1000px;
		border-radius: 10px;
		padding: 20px;
		background-color: white;
	}

	.header {
		display: flex;
		justify-content: space-between;
	}

	.header i {
		cursor: pointer;
	}

	.cookies h6 {
		color: #84bc22;
		padding-top: 2px;
		font-weight: bold;
	}
	.cookies p {
		font-size: 14px;
		line-height: 25px;
	}
	.cookies a {
		color: #84bc22;
		text-decoration: none;
	}
	
	.accept {
		display: block;
		color: #ffffff;
		background-color: #84bc22;
		border-radius: 16px;
		border: none;
		padding: 2px 20px;
		text-transform: uppercase;
		margin-left: auto;
	}
</style>
