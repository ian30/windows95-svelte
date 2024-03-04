<script>
	export let desktopBackgroundColor = '26726d';
</script>

<div class="desktop" style="background-color: #{desktopBackgroundColor}">
	<slot />
</div>

<style>
	.desktop {
		position: relative;
		width: 100%;
		height: 100vh;
		background-color: #f0f0f0;
		border: 1px solid #ccc;
		padding: 1rem;
	}
</style>
