<script lang="ts">
	// No $app/stores import needed for this simpler version

	const navLinks = [
		{ href: '/', label: 'Home' },
		{ href: '/projects', label: 'Projects' },
		{ href: '/education', label: 'Education' },
		{ href: '/contact', label: 'Contact' }
	];

	// For a very basic mobile menu toggle (optional, can be removed if too complex for now)
	let mobileMenuOpen = false;
	function toggleMobileMenu() {
		mobileMenuOpen = !mobileMenuOpen;
	}
</script>

<nav class="sticky top-0 z-50 bg-slate-800 text-white shadow-md">
	<div class="container mx-auto px-4 sm:px-6 lg:px-8">
		<div class="flex h-16 items-center justify-between">
			<!-- Logo/Brand -->
			<div class="flex-shrink-0">
				<a href="/" class="text-2xl font-bold transition-colors hover:text-sky-400">
					Ville Neuvonen
				</a>
			</div>

			<!-- Desktop Menu -->
			<div class="hidden items-baseline space-x-4 md:flex">
				{#each navLinks as link}
					<a
						href={link.href}
						class="rounded-md px-3 py-2 text-sm font-medium text-slate-300 transition-colors hover:bg-slate-700 hover:text-white"
					>
						{link.label}
					</a>
				{/each}
			</div>

			<!-- Mobile Menu Button (Simplified) -->
			<div class="flex items-center md:hidden">
				<button
					on:click={toggleMobileMenu}
					type="button"
					class="inline-flex items-center justify-center rounded-md p-2 text-slate-400 hover:bg-slate-700 hover:text-white focus:ring-2 focus:ring-white focus:outline-none focus:ring-inset"
					aria-expanded={mobileMenuOpen}
					aria-controls="mobile-menu-simple"
				>
					<span class="sr-only">Open main menu</span>
					<!-- Basic Menu Icon (can be replaced with SVG later) -->
					{#if !mobileMenuOpen}
						<svg
							class="block h-6 w-6"
							xmlns="http://www.w3.org/2000/svg"
							fill="none"
							viewBox="0 0 24 24"
							stroke-width="1.5"
							stroke="currentColor"
						>
							<path
								stroke-linecap="round"
								stroke-linejoin="round"
								d="M3.75 6.75h16.5M3.75 12h16.5m-16.5 5.25h16.5"
							/>
						</svg>
					{:else}
						<svg
							class="block h-6 w-6"
							xmlns="http://www.w3.org/2000/svg"
							fill="none"
							viewBox="0 0 24 24"
							stroke-width="1.5"
							stroke="currentColor"
						>
							<path stroke-linecap="round" stroke-linejoin="round" d="M6 18L18 6M6 6l12 12" />
						</svg>
					{/if}
				</button>
			</div>
		</div>
	</div>

	<!-- Mobile Menu (Simplified) -->
	{#if mobileMenuOpen}
		<div class="md:hidden" id="mobile-menu-simple">
			<div class="space-y-1 px-2 pt-2 pb-3 sm:px-3">
				{#each navLinks as link}
					<a
						href={link.href}
						class="block rounded-md px-3 py-2 text-base font-medium text-slate-300 transition-colors hover:bg-slate-700 hover:text-white"
						on:click={() => (mobileMenuOpen = false)}
					>
						{link.label}
					</a>
				{/each}
			</div>
		</div>
	{/if}
</nav>
