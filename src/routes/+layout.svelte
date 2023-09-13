<script>
	import '../app.css';
	import MonthlyImage from '$lib/MonthlyImage.svelte';
	import NavBar from '$lib/NavBar.svelte';
</script>

<!-- Layout with a full-screen background image, menubar and content panel at the center -->
<div>
	<MonthlyImage />
	<div>
		<NavBar />
	</div>
	<div>
		<slot />
	</div>
</div>
