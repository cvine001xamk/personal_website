<script lang="ts">
	import '../app.css';
	import Navbar from '../components/Navbar.svelte';
	import Footer from '../components/Footer.svelte';

	let { children } = $props();
</script>

<div
	class="flex min-h-screen flex-col bg-gray-100 text-gray-800 dark:bg-gray-900 dark:text-gray-200"
>
	<Navbar />
	{@render children()}
	<Footer />
</div>
