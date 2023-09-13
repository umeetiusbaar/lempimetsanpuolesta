<script>
	import '../app.css';
	import MonthlyImage from '$lib/MonthlyImage.svelte';
	import NavBar from '$lib/NavBar.svelte';
</script>

<!-- Layout with a full-screen background image, menubar and content panel at the center -->
<div class="h-screen flex flex-col">
	<MonthlyImage />
	<div>
		<NavBar />
	</div>
	<div class="flex-grow flex items-center justify-center">
		<slot />
	</div>
</div>
