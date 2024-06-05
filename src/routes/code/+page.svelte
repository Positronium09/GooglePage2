<script lang="ts">
	import LinkContainer from "../../linkContainer.svelte";

	let links: LinkData[] = new Array();
	links.push({
		displayName: "Github",
		url: "https://music.youtube.com/",
		color: "#F0FFFF"
	});
	links.push({
		displayName: "Stackoverflow",
		url: "https://mail.google.com/mail/",
		color: "#F6781D"
	});
</script>

<head>
	<title>Code</title>
</head>

<LinkContainer {links} />
