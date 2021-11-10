<script>
	import MenuItem from '../components/MenuItem.svelte';
	import menu from '../data/menu.json';
	import page from '../data/pages.json';
</script>

<main>
	<h1 class="section-title">{page.menu.title}</h1>
	<div class="section-intro">
		{page.menu.description}
	</div>
	{#each menu as item}
		<MenuItem {item} />
	{/each}
</main>
