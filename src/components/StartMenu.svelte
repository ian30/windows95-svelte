<script>
	import { writable } from 'svelte/store';
	export const startMenu = writable(false);

	function handleTopMenuClick() {
		console.log('click');
	}
	console.log('StartMenu.svelte file loaded');
</script>

<div class="startMenu" id="startMenu">
	<div class="startMenu__sidebar">
		<span>Windows</span>95
	</div>
	<div class="startMenu__items">
		<button class="startMenu__item isTopMenu" id="programs" on:click={handleTopMenuClick}>
			<img src="src/assets/icons/w95_programs.ico" alt="programs" />
			Programs
		</button>
		<button class="startMenu__item isTopMenu" id="documents" on:click={handleTopMenuClick}>
			<img src="src/assets/icons/w95_documents.ico" alt="documents" />
			Documents
		</button>
		<button class="startMenu__item isTopMenu" id="settings" on:click={handleTopMenuClick}>
			<img src="src/assets/icons/w95_settings.ico" alt="settings" />
			Settings
		</button>
		<button class="startMenu__item">
			<img src="src/assets/icons/w95_find.ico" alt="find" />
			Find
		</button>
		<button class="startMenu__item">
			<img src="src/assets/icons/w95_help.ico" alt="help" />
			Help
		</button>
		<button class="startMenu__item" id="run">
			<img src="src/assets/icons/w95_run.ico" alt="run" />
			Run
		</button>
		<hr />
		<div class="startMenu__item" id="logOff">
			<img src="src/assets/icons/w95_logoff.ico" alt="logOff" />Log Off
		</div>
		<div class="startMenu__item" id="shutDown">
			<img src="src/assets/icons/w95_shutdown.ico" alt="shutDown" />Shut Down
		</div>
	</div>
</div>

<style>
	hr {
		margin: 5px 0;
	}
	.startMenu {
		position: absolute;
		bottom: 40px;
		left: 0px;
		display: block;
		width: 300px;
		min-height: 400px;
		background-color: #bcbcbc;
		padding: 4px 4px 4px 4px;
		border: outset 3px #bababa;
	}
	.startMenu__sidebar {
		transform: rotate(-90deg);
		background-color: #9f9f9f;
		color: #fff;
		position: absolute;
		left: -209px;
		top: 196px;
		height: 43px;
		width: 148.3%;
		font-size: 300%;
		padding-left: 10px;
		opacity: 0.8;
		user-select: none;
	}
	.startMenu__sidebar span {
		font-family: 'Arial Black';
		opacity: 0.5;
	}
	.startMenu__items {
		user-select: none;
		width: 80%;
		margin-left: 40px;
	}
	.startMenu__item {
		padding: 10px 0 10px 3px;
		display: flex;
		flex-direction: row;
		align-items: flex-start;
		align-items: center;
		gap: 10px;
		width: 100%;
		border: none;
		background-color: transparent;
	}
	.startMenu__item:hover {
		background-color: blue;
		color: #fff;
	}
	.isTopMenu {
		position: relative;
	}
</style>
