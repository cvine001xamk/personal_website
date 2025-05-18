<script lang="ts">
	const currentYear = new Date().getFullYear();
</script>

<footer class="bg-slate-700 py-8 text-center text-slate-300">
	<div class="container mx-auto px-4">
		<p class="text-sm">
			© {currentYear} Ville Neuvonen. All rights reserved.
		</p>
		<p class="mt-2 text-xs">
			Built with <a
				href="https://kit.svelte.dev/"
				target="_blank"
				rel="noopener noreferrer"
				class="underline hover:text-sky-400">SvelteKit</a
			>
			and
			<a
				href="https://tailwindcss.com/"
				target="_blank"
				rel="noopener noreferrer"
				class="underline hover:text-sky-400">Tailwind CSS</a
			>.
		</p>
		<div class="mt-4 space-x-4">
			<a
				href="https://github.com/yourusername"
				target="_blank"
				rel="noopener noreferrer"
				class="hover:text-sky-400">GitHub</a
			>
			<a
				href="https://linkedin.com/in/yourusername"
				target="_blank"
				rel="noopener noreferrer"
				class="hover:text-sky-400">LinkedIn</a
			>
		</div>
	</div>
</footer>
