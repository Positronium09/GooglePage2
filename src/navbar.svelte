<script lang="ts">
	import { page, navigating } from "$app/stores";

	$: if ($navigating) {
		let path = $page.url.pathname;
		let navbar = document.getElementById("navbar");

		if (navbar != null) {
			if (path == "/main") {
				navbar.style.setProperty(
					"--background-gradient",
					"linear-gradient(125.31deg, #f2015b 0%, #ed02f1 47.92%, #0b0bfc 100%)"
				);
			} else if (path == "/code") {
				navbar.style.setProperty(
					"--background-gradient",
					"linear-gradient(to right, hsla(152, 100%, 50%, 1) 0%, hsla(186, 100%, 69%, 1) 100%)"
				);
			} else if (path == "/math") {
				navbar.style.setProperty(
					"--background-gradient",
					"linear-gradient(to right, #00d2ff, #5fa1ff)"
				);
			}
		}
	}
</script>

<nav id="navbar">
	<a
		aria-current={$page.url.pathname == "/main" ? "page" : undefined}
		href="/main">
		Main
	</a>
	<a
		aria-current={$page.url.pathname == "/code" ? "page" : undefined}
		href="/code">
		Code
	</a>
	<a
		aria-current={$page.url.pathname == "/math" ? "page" : undefined}
		href="/math">
		Math
	</a>
</nav>

<style>
	#navbar {
		--background-gradient: linear-gradient(
			125.31deg,
			#f2015b 0%,
			#ed02f1 47.92%,
			#0b0bfc 100%
		);

		display: flex;
		align-items: center;
		justify-content: center;
		gap: 100px;

		position: relative;

		height: 100px;
	}

	#navbar::after {
		content: "";
		width: 100%;
		height: 3px;

		background: var(--background-gradient);

		position: absolute;
		bottom: -2px;
		left: 0;
	}

	#navbar a {
		color: aliceblue;
		text-decoration: none;
		font-size: 32px;
		position: relative;
	}

	#navbar > a[aria-current="page"]::after {
		content: "";
		width: 100%;
		height: 1px;

		background: aliceblue;

		position: absolute;
		bottom: -2px;
		left: 0;
	}
</style>
