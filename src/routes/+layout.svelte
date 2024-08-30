<script lang="ts">
	import '../app.css';
	import Navbar from '$lib/NavBar.svelte';
	import Footer from '$lib/Footer.svelte';
</script>

<svelte:head>
	<base href="/fea-dev-website/" />
</svelte:head>

<Navbar />
<slot></slot>
<Footer />

<style>
	:global(body) {
		margin: 0;
		padding: 0;
		overflow-x: hidden;
	}
</style>
