<script>
    import Breadcrumb from '$lib/nav/Breadcrumb.svelte';
</script>

<nav aria-label="breadcrumb" class="mt-2 mt-lg-4">
    <ol class="breadcrumb">
        <Breadcrumb href="/" name="Home" />
      <slot />
    </ol>
</nav>

<style>
    nav {
        display: flex;
        justify-content: center;
    }
</style>
