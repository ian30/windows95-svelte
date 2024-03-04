<script>
	import StartMenu from './StartMenu.svelte';
	import { writable } from 'svelte/store';
	export const startMenu = writable(false);
	function toggleStartMenu() {
		document.getElementById('startButton')?.classList.toggle('notActive');
		startMenu.update((value) => !value);
	}
</script>

<button type="button" class="startButton notActive" id="startButton" on:click={toggleStartMenu}>
	<img src="src/assets/icons/w95_mslogo.ico" alt="Start" />
	<span>Start</span>
</button>

{#if $startMenu}
	<StartMenu />
{/if}

<style>
	.startButton {
		width: 70px;
		padding: 4px;
		border: inset 3px #ddd;
		height: 35px;
		display: flex;
		align-items: center;
		justify-content: space-between;
		cursor: default;
		user-select: none;
		background-color: #c5c5c5;
	}
	.startButton img {
		width: 26px;
		font-weight: bold;
	}
	.startButton span {
		font-weight: bold;
	}
	.startButton.notActive {
		background-color: #bababa;
		border: outset 3px #ddd;
	}
</style>
