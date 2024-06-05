<script lang="ts">
	import LinkContainer from "../../linkContainer.svelte";

	let links: LinkData[] = new Array();
	links.push({
		displayName: "WolframAlpha",
		url: "https://wolfreealpha.netlify.app/input/",
		color: "#FFBF00"
	});
	links.push({
		displayName: "Desmos",
		url: "https://www.desmos.com/calculator?lang=en",
		color: "#66FF00"
	});
	links.push({
		displayName: "Desmos 3D",
		url: "https://www.desmos.com/3d",
		color: "#66FF00"
	});
</script>

<head>
	<title>Math</title>
</head>

<LinkContainer {links} />
