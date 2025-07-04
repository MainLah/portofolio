<script lang="ts">
	import Marquee from 'svelte-fast-marquee';
	import Projects from '$lib/components/projects.svelte';
	import { tools1, tools2, projects, contacts } from '$lib';
</script>

<section id="home" class="flex min-h-screen items-center justify-center">
	<div
		class="relative h-[calc(100vh-1rem)] w-[calc(100vw-1.5rem)] overflow-hidden rounded-[3rem] bg-amber-200 shadow-xl"
	>
		<div class="pointer-events-none absolute inset-0 hidden select-none md:block">
			{#each Array(10) as _}
				<h1
					class="w-full text-center text-[6vw] tracking-[2rem] whitespace-nowrap text-black/10 lg:text-[5vw]/none"
				>
					RTFOLIOPORTFOLIOPORTFOLIOPORTFOLIOPORTFOLIOPORTFOLIO
				</h1>
			{/each}
		</div>
		<div class="relative z-10 flex flex-col items-center justify-center py-16 md:py-32">
			<h1
				class="xs:text-4xl text-center text-3xl leading-tight font-extrabold tracking-tight text-black drop-shadow-md sm:text-5xl md:text-6xl lg:text-7xl"
			>
				RENDRA KUSUMA B
			</h1>
			<h2
				class="xs:text-2xl mt-4 text-center text-xl font-semibold tracking-wide text-black drop-shadow sm:text-3xl md:text-4xl lg:text-5xl"
			>
				A WEB DEVELOPER
			</h2>
		</div>
	</div>
</section>
<section id="about" class="flex min-h-screen flex-col items-center justify-center gap-16 pt-48">
	<div class="flex w-full flex-col items-center gap-5">
		<div class="flex w-2/5 justify-between">
			<h1 class="text-8xl font-bold text-amber-200">about</h1>
			<div class="group -mt-10 flex items-center">
				<a
					href="https://drive.google.com/file/d/13mZvF7givtMcR36J0V1Cc3nkM1nXLmv0/view?usp=sharing"
					target="_blank"
					class="inline rounded-[2rem] border border-amber-200 px-6 py-3 text-lg text-amber-200 group-hover:bg-lime-900"
				>
					Curriculum Vitae
				</a>

				<span
					class="rotate-z-90 cursor-pointer rounded-full border border-amber-200 px-3 py-3 group-hover:bg-lime-900"
				>
					<svg
						xmlns="http://www.w3.org/2000/svg"
						width="24"
						height="24"
						viewBox="0 0 24 24"
						fill="none"
						stroke="#fee685"
						stroke-width="2"
						stroke-linecap="round"
						stroke-linejoin="round"
						class="lucide lucide-arrow-up-left-icon lucide-arrow-up-left"
						><path d="M7 17V7h10" /><path d="M17 17 7 7" /></svg
					>
				</span>
			</div>
		</div>
		<div class="flex w-1/3 justify-end">
			<p class="w-3/5 text-lg text-amber-200">
				Welcome to my portfolio. I am Rendra Kusuma Blikololo, a fullstack developer who loves
				learning new technologies.
			</p>
		</div>
	</div>
	<div class="w-full">
		<div class="h-[50vh] w-full">
			<Marquee speed={60} play={true}>
				{#each tools1 as icon}
					<img src={icon} alt={icon} width="150" class="mx-25 my-4" />
				{/each}
			</Marquee>
			<Marquee speed={60} play={true} direction="right">
				{#each tools2 as icon}
					<img src={icon} alt={icon} width="150" class="mx-25 my-4" />
				{/each}
			</Marquee>
		</div>
	</div>
</section>
<section id="projects" class="mt-16 flex min-h-screen flex-col items-center justify-center gap-16">
	<div class="flex w-full justify-center gap-32">
		<div class="group mt-26 flex items-center">
			<a
				href="https://github.com/MainLah"
				target="_blank"
				class="inline rounded-[2rem] border border-amber-200 px-6 py-3 text-lg text-amber-200 group-hover:bg-lime-900"
			>
				View All
			</a>

			<span
				class="rotate-z-90 cursor-pointer rounded-full border border-amber-200 px-3 py-3 group-hover:bg-lime-900"
			>
				<svg
					xmlns="http://www.w3.org/2000/svg"
					width="24"
					height="24"
					viewBox="0 0 24 24"
					fill="none"
					stroke="#fee685"
					stroke-width="2"
					stroke-linecap="round"
					stroke-linejoin="round"
					class="lucide lucide-arrow-up-left-icon lucide-arrow-up-left"
					><path d="M7 17V7h10" /><path d="M17 17 7 7" /></svg
				>
			</span>
		</div>
		<div class="flex flex-col items-end text-end">
			<h1 class="pb-6 text-8xl font-bold text-amber-200">projects</h1>
			<p class="w-3/5 text-lg text-amber-200">
				Browse through a variety of works that I have done in the past.
			</p>
		</div>
	</div>
	<div class="my-8 flex w-full flex-col items-center">
		{#each projects as project}
			<Projects
				year={project.year}
				name={project.name}
				description={project.description}
				href={project.href}
				className={project?.className}
			/>
		{/each}
	</div>
</section>
<section id="contacts" class="flex min-h-screen items-center justify-center">
	<div
		class="relative h-[calc(100vh-1rem)] w-[calc(100vw-1.5rem)] overflow-hidden rounded-[3rem] bg-amber-200 shadow-xl"
	>
		<div class="pointer-events-none absolute inset-0 hidden select-none md:block">
			{#each Array(10) as _}
				<h1
					class="w-full text-center text-[6vw] tracking-[2rem] whitespace-nowrap text-black/10 lg:text-[5vw]/none"
				>
					RTFOLIOPORTFOLIOPORTFOLIOPORTFOLIOPORTFOLIOPORTFOLIO
				</h1>
			{/each}
		</div>
		<div class="relative z-10 flex flex-col items-center justify-center py-16 md:py-32">
			<h1
				class="xs:text-4xl text-center text-3xl leading-tight font-extrabold tracking-tight text-black drop-shadow-md sm:text-5xl md:text-6xl lg:text-7xl"
			>
				CONTACT ME
			</h1>
		</div>
		<div class="relative z-100 flex w-full justify-center">
			<div class="h-[10vh] max-w-screen-sm">
				<div
					class="flex h-full w-full items-center justify-evenly gap-16 rounded-xl bg-lime-900 px-8"
				>
					{#each contacts as contact}
						<a href={contact.href} class="duration-100 hover:-translate-y-4">
							<img
								src={contact.svg}
								alt={contact.alt}
								width={contact.alt.toLowerCase() === 'linkedin' ? '90' : '60'}
							/>
						</a>
					{/each}
				</div>
			</div>
		</div>
	</div>
</section>
