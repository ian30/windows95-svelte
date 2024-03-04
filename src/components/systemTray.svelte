<script>
	import { onMount } from 'svelte';
	let clockDsp = '';

	function updateClock() {
		const now = new Date();
		const hours = now.getHours();
		const minutes = now.getMinutes();
		const seconds = now.getSeconds();

		clockDsp = `${hours.toString().padStart(2, '0')}:${minutes.toString().padStart(2, '0')}`;
	}
	onMount(() => {
		updateClock();
		const interval = setInterval(updateClock, 1000);

		return () => {
			clearInterval(interval);
		};
	});
</script>

<div class="systemTray">
	<div class="systemTray__item" id="sysTrayClock">{clockDsp}</div>
</div>

<style>
	.systemTray {
		border: inset 2px #bababa;
		display: flex;
		gap: 10px;
		align-items: center;
		padding: 0 12px;
	}
</style>
