<script>
	import '$lib/global.css';
	import Icon from '../components/Icon.svelte';
	import StartButton from '../components/StartButton.svelte';
	import SystemTray from '../components/systemTray.svelte';
	import Taskbar from '../components/Taskbar.svelte';
	import Desktop from '../components/Desktop.svelte';
</script>

<Desktop>
	<Icon app__name="My Computer" icon__path="src/assets/icons/my_computer.png" icon__width="64px" />
	<Icon
		app__name="My Computer"
		icon__path="src/assets/icons/recycle_bin_empty.png"
		icon__width="64px"
	/>
	<Icon app__name="Network" icon__path="/src/assets/icons/w95_network.ico" />
	<Taskbar>
		<StartButton />
		<SystemTray />
	</Taskbar>
</Desktop>
