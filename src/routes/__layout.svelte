<script>
	import Navbar from '$lib/nav/Navbar.svelte';
	import Footer from '$lib/nav/Footer.svelte';

    import '../app.css';
</script>

<Navbar />

<div class="container-xl">
	<slot />
</div>

<Footer />

<!--change body color; 
	
-->