<script>
	let socials = [
		{ icon: 'facebook', href: 'https://www.facebook.com/OSFGlobalServices/' },
		{ icon: 'google', href: 'https://www.google.com' },
		{ icon: 'twitter', href: 'https://twitter.com/osfglobal' },
		{ icon: 'pinterest', href: 'https://www.pinterest.ca/osfglobal/' }
	];
</script>

{#each socials as { icon, href }}
	<a {href} target="_blank">
		<i class="bi bi-{icon}" />
	</a>
{/each}

<style>
	a {
		text-decoration: none;
		padding: 0 5px;
	}
	i {
		color: #7d7a77;
	}
</style>
