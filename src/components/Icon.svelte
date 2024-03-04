<script>
	export let app__name = 'default';
	export let icon__path = 'src/assets/icons/w95_default.ico';
	export let icon__width = '48px';
</script>

<div class="icon" draggable="true">
	<div class="icon__img"><img src={icon__path} alt="icon" width={icon__width} /></div>
	<div class="icon__label">{app__name}</div>
</div>

<style>
	.icon {
		width: 84px;
		height: 64px;
		position: relative;
		margin-bottom: 20px;
	}
	.icon:active {
		border-radius: 5px;
		border: 1px dashed rgba(220, 220, 220, 0.6);
	}
	.icon__img {
		position: absolute;
		top: -10px;
		border-radius: 4px;
	}
	.icon__label {
		position: absolute;
		bottom: 0;
		text-align: center;
	}
</style>
