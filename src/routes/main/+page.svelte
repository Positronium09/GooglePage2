<script lang="ts">
	import LinkContainer from "../../linkContainer.svelte";

	let links: LinkData[] = new Array();
	links.push({
		displayName: "Youtube",
		url: "https://youtube.com/",
		color: "#FE0000"
	});
	links.push({
		displayName: "YT Music",
		url: "https://music.youtube.com/",
		color: "#FE0000"
	});
	links.push({
		displayName: "Mail",
		url: "https://mail.google.com/mail/",
		color: "#F20131"
	});
	links.push({
		displayName: "Yaşar OBS",
		url: "https://obs.yasar.edu.tr/oibs/std/login.aspx",
		color: "#5080CC"
	});
	links.push({
		displayName: "Yaşar Software Announcements",
		url: "https://se.yasar.edu.tr/category/bolum-duyurulari/",
		color: "#5080CC"
	});
</script>

<head>
	<title>Main</title>
</head>

<LinkContainer {links} />
