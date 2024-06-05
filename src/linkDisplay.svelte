<script lang="ts">
	import { onMount } from "svelte";

	export let displayName;
	export let url;
	export let color;

	let linkElement: HTMLAnchorElement;

	onMount(() => {
		linkElement.style.setProperty("--link-color", color);
	});
</script>

<a href={url} class="link" bind:this={linkElement}>
	<div class="link-container">
		<p class="link-name">{displayName}</p>
	</div>
</a>

<style>
	.link {
		border: 2px solid #272727;
		color: #454545;
		text-decoration: none;
		transition:
			border-color 150ms,
			color 150ms;
		border-radius: 10px;
	}

	.link:hover {
		color: var(--link-color);
		border-color: var(--link-color);
	}

	.link-container {
		min-width: 200px;
		padding-left: 50px;
		padding-right: 50px;
		height: 85px;
		display: flex;
		justify-content: center;
		align-items: center;
	}

	.link-name {
		font-weight: 400;
		font-size: x-large;
	}
</style>
