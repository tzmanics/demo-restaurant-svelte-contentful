<script>
	export let item;
</script>

<section class="menu-item">
	<div class="menu-item-header">
		<h2 class="menu-item-title">{item.title}</h2>
		<span class="menu-item-price">{item.currency}{item.price}</span>
	</div>
	<p class="menu-item-description" />
	<p class="menu-item-description">{item.description}</p>
	{#if item.photo.imageUrl}
		<figure>
			<img src={item.photo.imageUrl} alt={item.photo.caption} />
			<figcaption>
				{item.photo.caption} — <a href={item.photo.attribution.url}>Photo credit</a>
			</figcaption>
		</figure>
	{/if}
</section>

<style>
	.menu-item {
		margin-bottom: 6rem;
	}
	.menu-item-description {
		margin: 0;
	}
	.menu-item img {
		width: 100%;
		background-color: #fff;
		padding: 1rem;
		margin: 1rem -1rem 0;
		box-shadow: 0 3px 6px #0004;
	}
	.menu-item figcaption {
		text-align: center;
		font-size: 0.9rem;
		margin-top: 0.5em;
	}
	.menu-item-header {
		display: flex;
		align-items: center;
		margin-bottom: 10px;
	}
	.menu-item-price {
		font-size: 1rem;
		margin-left: 1em;
	}
	.menu-item-title {
		margin: 0;
		font-size: 20px;
	}
</style>
