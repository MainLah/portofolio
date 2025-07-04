<script lang="ts">
	import Marquee from 'svelte-fast-marquee';
	import Projects from '$lib/components/projects.svelte';
	import { tools1, tools2, projects, contacts } from '$lib';
</script>

<section id="home" class="flex items-center justify-center md:min-h-screen">
	<div
		class="relative my-8 w-[calc(100vw-1.5rem)] overflow-hidden rounded-[3rem] bg-amber-200 shadow-xl md:my-0 md:h-[calc(100vh-1rem)]"
	>
		<div class="pointer-events-none absolute inset-0 block select-none">
			{#each Array(30) as _}
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
			<img
				src="down-sm-svgrepo-com.svg"
				alt="Scroll Down"
				class="mt-48 w-[100px] animate-bounce md:w-[160px]"
			/>
		</div>
	</div>
</section>
<section
	id="about"
	class="flex flex-col items-center justify-center gap-16 pt-12 md:min-h-screen md:pt-48"
>
	<div class="flex w-full flex-col items-center gap-5">
		<div
			class="flex w-full flex-col items-center justify-between md:w-2/5 md:flex-row md:items-start"
		>
			<h1 class="text-7xl font-bold text-amber-200 md:text-8xl">about</h1>
			<div class="group flex items-center md:-mt-10">
				<a
					href="https://drive.google.com/file/d/13mZvF7givtMcR36J0V1Cc3nkM1nXLmv0/view?usp=sharing"
					target="_blank"
					class="text-md inline rounded-[2rem] border border-amber-200 px-3 py-1 text-nowrap text-amber-200 group-hover:bg-lime-900 md:px-6 md:py-3 md:text-lg"
				>
					Curriculum Vitae
				</a>

				<span
					class="rotate-z-90 cursor-pointer rounded-full border border-amber-200 p-1 group-hover:bg-lime-900 md:px-3 md:py-3"
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
		<div class="flex w-full md:w-1/3 md:justify-end">
			<p class="w-full text-center text-lg text-amber-200 md:w-3/5 md:text-start">
				Welcome to my portfolio. I am Rendra Kusuma Blikololo, a fullstack developer who loves
				learning new technologies.
			</p>
		</div>
	</div>
	<div class="w-full">
		<div class="mb-16 w-full md:h-[50vh]">
			<Marquee speed={60} play={true}>
				{#each tools1 as icon}
					<img src={icon} alt={icon} class="mx-5 my-4 w-[50px] md:mx-25 md:w-[150px]" />
				{/each}
			</Marquee>
			<Marquee speed={60} play={true} direction="right">
				{#each tools2 as icon}
					<img src={icon} alt={icon} class="mx-5 my-4 w-[50px] md:mx-25 md:w-[150px]" />
				{/each}
			</Marquee>
		</div>
	</div>
</section>
<section
	id="projects"
	class="flex min-h-screen flex-col items-center justify-center gap-16 md:mt-16"
>
	<div class="flex w-full flex-col justify-center gap-4 md:flex-row md:gap-32">
		<div class="group hidden items-center justify-center md:mt-26 md:flex md:justify-start">
			<a
				href="https://github.com/MainLah"
				target="_blank"
				class="rounded-[2rem] border border-amber-200 px-3 py-1 text-lg text-amber-200 group-hover:bg-lime-900 md:px-6 md:py-3"
			>
				View All
			</a>

			<span
				class="rotate-z-90 cursor-pointer rounded-full border border-amber-200 p-1 group-hover:bg-lime-900 md:px-3 md:py-3"
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
		<div class="flex flex-col items-center md:items-end md:text-end">
			<h1 class="pb-3 text-7xl font-bold text-amber-200 md:pb-6 md:text-8xl">projects</h1>
			<div class="group mb-4 flex items-center justify-center md:mt-26 md:hidden md:justify-start">
				<a
					href="https://github.com/MainLah"
					target="_blank"
					class="rounded-[2rem] border border-amber-200 px-3 py-1 text-lg text-amber-200 group-hover:bg-lime-900 md:px-6 md:py-3"
				>
					View All
				</a>

				<span
					class="rotate-z-90 cursor-pointer rounded-full border border-amber-200 p-1 group-hover:bg-lime-900 md:px-3 md:py-3"
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
			<p class="w-full text-center text-lg text-amber-200 md:w-3/5 md:text-start">
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
<section id="contacts" class="flex items-center justify-center md:min-h-screen">
	<div
		class="relative my-8 w-[calc(100vw-1.5rem)] overflow-hidden rounded-[3rem] bg-amber-200 py-12 shadow-xl md:my-0 md:h-[calc(100vh-1rem)]"
	>
		<div class="pointer-events-none absolute inset-0 block select-none">
			{#each Array(30) as _}
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
		<div class="relative z-100 my-8 flex w-full justify-center">
			<div class="h-full max-w-screen-sm md:h-[10vh]">
				<div
					class="flex h-full w-full flex-row items-center justify-evenly gap-8 rounded-xl bg-lime-950 px-4 py-2 md:gap-16 md:px-8 md:py-12"
				>
					{#each contacts as contact}
						<a href={contact.href} class="duration-100 hover:-translate-y-4">
							<img src={contact.svg} alt={contact.alt} class="size-[30px] md:size-[60px]" />
						</a>
					{/each}
				</div>
			</div>
		</div>
	</div>
</section>
