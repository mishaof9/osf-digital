<script>
    import Breadcrumb from '$lib/nav/Breadcrumb.svelte';
</script>

<nav aria-label="breadcrumb" class="mt-3 mt-lg-5">
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
