<script>
export let show;
	function handleKeydown(event) {
		if (event.key == 'Escape') show = false;
    }
</script>
<svelte:window on:keydown={handleKeydown} />
<!-- cookies form starts here -->
<div class="cookies class:hidden={!show} on:click|self={() => (show = false)}">
	<div class="subwrapper">
		<h6>This website uses cookies</h6>
		<p>
			OSF uses its own and third-party cookies for statistical purposes, to know your preferences,
			for website performance <br> and interaction with social media offering publicity tailored to your
			interests. If you continue browsing, we consider that you accept its use.<br />
			You can expand this information consulting our <a href="#">Cookies Policy Page</a>.
			<span id="close-cookies"><i class="fas fa-times" /></span>
		</p>
		<button class="accept-cookies btn">Accept</button>
	</div>
</div>

<style>
	.hidden {
		display: none;
	}
    .cookies {
		position: absolute;
		top: 0;
		left: 0;
		width: 100vw;
		height: 100vh;
		background-color: rgba(100, 100, 100, 0.5);
		z-index: 1;
	}
    .subwrapper {
		position: absolute;
		width: 1170px;
		height: 145px;
		text-align:left;
		border-radius: 10px;
		padding: 10px;
		background-color: white;
		
	}
    .subwrapper h6{
        color:#84bc22;
        font-family: Lato, sans-serif;
        font-size: 16px;
        font-weight: bold;
    }
    .subwrapper p{
        font-family: Lato, sans-serif;
        font-size:14px;
    }
    .subwrapper a {
        color: #84bc22;
        text-decoration: none;
    }
    .accept-cookies{
        color: #ffffff;
		background-color: #84bc22;
        border-radius: 16px;
        padding: 2px 20px;
        text-transform: uppercase;
        

    }
</style>
