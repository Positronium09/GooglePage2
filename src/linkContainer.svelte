<script lang="ts">
	import LinkDisplay from "./linkDisplay.svelte";

	export let links: LinkData[];
</script>

<div id="link-container">
	{#each links as link}
		<LinkDisplay
			displayName={link.displayName}
			url={link.url}
			color={link.color} />
	{/each}
</div>

<style>
	#link-container {
		margin: 100px;

		display: flex;
		flex-wrap: wrap;
		gap: 50px;

		justify-content: center;
		font-weight: normal;
	}
</style>
