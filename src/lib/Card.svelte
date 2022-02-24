<script>
    export let height = 365;
</script>

<div style:height="{height}px">
    <slot />
</div>

<style>
	div {
		display: inline-block;
		width: 270px;
		margin: 15px;
		overflow: hidden;

		border: none;
		border-radius: 5px;

		background: white;

		font-size: 15px;
		line-height: 15px;
		letter-spacing: 1px;
		text-align: center;
		color: black;

        position: relative;
	}
</style>
