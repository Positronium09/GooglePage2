<script>
	import Navbar from "../navbar.svelte";
	import WeatherInfo from "../weatherInfo.svelte";
</script>

<div id="content-container">
	<header>
		<Navbar />
	</header>

	<main>
		<slot />
	</main>

	<!-- <footer>
		<WeatherInfo />
	</footer> -->
</div>

<style>
	@import url("https://fonts.googleapis.com/css2?family=Roboto+Mono:ital,wght@0,100..700;1,100..700&display=swap");

	:root {
		font-family: "Roboto Mono", monospace;
		font-optical-sizing: auto;
		font-weight: lighter;

		color: aliceblue;
		background-color: #111111;
	}

	#content-container {
		display: flex;
		flex-direction: column;
		height: 100vh;
	}

	main {
		margin-top: 5px;
		margin-bottom: 5px;
		flex-grow: 1;
		padding: 8px;
		overflow-y: auto;
		scrollbar-width: 10px;
		scrollbar-color: #1b1b1b #303030;
	}

	/* main::-webkit-scrollbar {
		width: 10px;
	}

	main::-webkit-scrollbar-track {
		background: #212121;
		border-top-right-radius: 5px;
		border-bottom-right-radius: 5px;
	}

	main::-webkit-scrollbar-thumb {
		border-radius: 10px;
		border-color: red;
		background: transparent;
	}

	main::-webkit-scrollbar-thumb:hover {
		background: #555;
	} */
</style>
