<!-- A navigation bar that is slightly transparent and contains links for Home (on the left), Info, Media and Gallery (on the right). Menu links are as text (e.g. "Info") except for home which is always an icon. -->
<script>
	import { onMount } from 'svelte';

	export let links = [
		{
			name: 'Koti',
			path: '/',
			icon: 'home'
		},
		{
			name: 'Info',
			path: '/info',
			icon: 'info'
		},
		{
			name: 'Media',
			path: '/media',
			icon: 'newspaper'
		},
		{
			name: 'Galleria',
			path: '/gallery',
			icon: 'images'
		}
	];

	let isMobile = false;

	onMount(() => {
		isMobile = window.matchMedia('(max-width: 768px)').matches;
	});
</script>

<div class="pt-4 pb-4 pr-0 pl-0 bg-white opacity-75">
	<ul class="flex justify-between items-center">
		<li class="ml-4">
			<a href={links[0].path}>
				{#if !isMobile}
					{links[0].name}
				{/if}
				<i class="fas fa-{links[0].icon}" />
			</a>
		</li>
		<div class="flex items-center">
			{#each links.slice(1) as link}
				<li class="ml-4 pr-4">
					<a href={link.path}>
						{#if !isMobile}
							{link.name}
						{/if}
						<i class="fas fa-{link.icon}" />
					</a>
				</li>
			{/each}
		</div>
	</ul>
</div>
