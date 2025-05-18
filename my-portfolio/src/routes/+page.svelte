<script lang="ts">
	// You can import project data or other things here later
</script>

<svelte:head>
	<title>Ville Neuvonen - Software Engineering Student</title>
	<meta
		name="description"
		content="Welcome to the portfolio of [Your Name], a passionate software engineering student showcasing projects and skills."
	/>
</svelte:head>

<section id="hero" class="py-16 text-center md:py-24">
	<img
		src="/profile.jpg"
		alt="Ville Neuvonen"
		class="mx-auto mb-6 h-32 w-32 rounded-full border-4 border-sky-500 shadow-lg md:h-40 md:w-40"
	/>
	<h1 class="mb-4 text-4xl font-bold text-slate-900 md:text-5xl dark:text-white">
		Hi, I'm <span class="text-sky-500 dark:text-sky-400">Ville Neuvonen</span>
	</h1>
	<p class="mx-auto mb-8 max-w-2xl text-xl text-slate-700 md:text-2xl dark:text-slate-300">
		A passionate Software Engineering Student specializing in [Your Specialization, e.g., Web
		Development, AI, etc.]. Currently exploring innovative solutions and building cool stuff.
	</p>
	<div class="space-x-4">
		<a
			href="/projects"
			class="rounded-lg bg-sky-500 px-6 py-3 font-semibold text-white shadow-md transition-colors hover:bg-sky-600"
		>
			View My Projects
		</a>
		<a
			href="/contact"
			class="rounded-lg bg-slate-600 px-6 py-3 font-semibold text-white shadow-md transition-colors hover:bg-slate-700"
		>
			Get In Touch
		</a>
	</div>
</section>

<section
	id="about-short"
	class="my-12 rounded-lg bg-white py-16 shadow-xl md:py-20 dark:bg-slate-800"
>
	<div class="container mx-auto px-6 lg:px-8">
		<h2 class="mb-10 text-center text-3xl font-bold text-slate-900 dark:text-white">
			A Little About Me
		</h2>
		<p class="mx-auto mb-6 max-w-3xl text-lg leading-relaxed text-slate-700 dark:text-slate-300">
			I am currently pursuing my degree in Software Engineering at [Your University Name]. My
			journey in tech is driven by a curiosity to understand how things work and a desire to create
			software that solves real-world problems. I'm particularly interested in [Mention 1-2 areas
			like: full-stack development, cloud technologies, machine learning].
		</p>
		<p class="mx-auto max-w-3xl text-lg leading-relaxed text-slate-700 dark:text-slate-300">
			When I'm not coding, you might find me [Your Hobby 1, e.g., exploring new hiking trails,
			reading sci-fi novels, or contributing to open-source projects].
		</p>
	</div>
</section>

<section id="skills-overview" class="py-16 md:py-20">
	<div class="container mx-auto px-6 lg:px-8">
		<h2 class="mb-12 text-center text-3xl font-bold text-slate-900 dark:text-white">Key Skills</h2>
		<div
			class="mx-auto grid max-w-4xl grid-cols-2 gap-6 text-center sm:grid-cols-3 md:grid-cols-4 lg:grid-cols-5"
		>
			{#each ['JavaScript', 'TypeScript', 'SvelteKit', 'Node.js', 'Python', 'SQL', 'Git', 'Docker', 'React', 'Tailwind CSS'] as skill}
				<div class="rounded-lg bg-slate-100 p-4 shadow-md dark:bg-slate-700">
					<p class="font-semibold text-slate-800 dark:text-slate-200">{skill}</p>
				</div>
			{/each}
		</div>
		<p class="mt-8 text-center text-slate-600 dark:text-slate-400">
			...and always eager to learn more!
		</p>
	</div>
</section>
