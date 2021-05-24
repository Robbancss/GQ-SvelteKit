<script lang="ts">
	import Header from '$lib/Header/index.svelte';
	import Footer from '$lib/Footer/index.svelte';
	import LeftSidebar from '$lib/Left-Sidebar/index.svelte';
	import RightSidebar from '$lib/Right-Sidebar/index.svelte';
	import '../app.css';
</script>

<div class="layout">
	<header>
		<Header />
	</header>

	<div class="left-sidebar">
		<LeftSidebar />
	</div>

	<main>
		<slot />
	</main>

	<div class="right-sidebar">
		<RightSidebar />
	</div>

	<footer>
		<Footer />
	</footer>
</div>

<style>
	.layout {
		display: grid;
		height: 100vh;
		grid-template: auto 1fr auto / auto 1fr auto;
		margin: 0 auto;
	}

	header {
		background: lightpink;
		grid-column: 1 / 4;
	}

	.left-sidebar {
		background: lightblue;
		grid-column: 1 / 2;
	}

	main {
		background: coral;
		grid-column: 2 / 3;
	}

	.right-sidebar {
		background: yellow;
		grid-column: 3 / 4;
	}

	footer {
		background: wheat;
		grid-column: 1 / 4;
	}
</style>
