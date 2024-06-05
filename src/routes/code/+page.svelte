<script lang="ts">
	import LinkContainer from "../../linkContainer.svelte";

	let links: LinkData[] = new Array();
	links.push({
		displayName: "Github",
		url: "https://github.com/",
		color: "#F0FFFF"
	});
	links.push({
		displayName: "Stackoverflow",
		url: "https://stackoverflow.com/",
		color: "#F6781D"
	});
</script>

<head>
	<title>Code</title>
</head>

<LinkContainer {links} />
