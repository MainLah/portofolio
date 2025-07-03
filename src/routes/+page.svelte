<script lang="ts">
	import Marquee from 'svelte-fast-marquee';
	const tools1 = [
		'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/svelte/svelte-original.svg',
		'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/react/react-original.svg',
		'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/nextjs/nextjs-original.svg',
		'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/supabase/supabase-original.svg',
		'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/mongodb/mongodb-original.svg'
	];
	const tools2 = [
		'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/javascript/javascript-original.svg',
		'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/typescript/typescript-original.svg',
		'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/nodejs/nodejs-original.svg',
		'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/express/express-original.svg',
		'https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/laravel/laravel-original.svg'
	];
</script>

<section id="home" class="flex min-h-screen items-center justify-center">
	<div
		class="relative h-[calc(100vh-1rem)] w-[calc(100vw-1.5rem)] overflow-hidden rounded-[3rem] bg-amber-200 shadow-xl"
	>
		<div class="pointer-events-none absolute inset-0 hidden select-none md:block">
			<h1
				class="w-full text-center text-[6vw] tracking-[2rem] whitespace-nowrap text-black/10 lg:text-[5vw]/none"
			>
				RTFOLIOPORTFOLIOPORTFOLIOPORTFOLIOPORTFOLIOPORTFOLIO
			</h1>
			<h1
				class="w-full text-center text-[6vw] tracking-[2rem] whitespace-nowrap text-black/10 lg:text-[5vw]/none"
			>
				RTFOLIOPORTFOLIOPORTFOLIOPORTFOLIOPORTFOLIOPORTFOLIO
			</h1>
			<h1
				class="w-full text-center text-[6vw] tracking-[2rem] whitespace-nowrap text-black/10 lg:text-[5vw]/none"
			>
				RTFOLIOPORTFOLIOPORTFOLIOPORTFOLIOPORTFOLIOPORTFOLIO
			</h1>
			<h1
				class="w-full text-center text-[6vw] tracking-[2rem] whitespace-nowrap text-black/10 lg:text-[5vw]/none"
			>
				RTFOLIOPORTFOLIOPORTFOLIOPORTFOLIOPORTFOLIOPORTFOLIO
			</h1>
			<h1
				class="w-full text-center text-[6vw] tracking-[2rem] whitespace-nowrap text-black/10 lg:text-[5vw]/none"
			>
				RTFOLIOPORTFOLIOPORTFOLIOPORTFOLIOPORTFOLIOPORTFOLIO
			</h1>
			<h1
				class="w-full text-center text-[6vw] tracking-[2rem] whitespace-nowrap text-black/10 lg:text-[5vw]/none"
			>
				RTFOLIOPORTFOLIOPORTFOLIOPORTFOLIOPORTFOLIOPORTFOLIO
			</h1>
			<h1
				class="w-full text-center text-[6vw] tracking-[2rem] whitespace-nowrap text-black/10 lg:text-[5vw]/none"
			>
				RTFOLIOPORTFOLIOPORTFOLIOPORTFOLIOPORTFOLIOPORTFOLIO
			</h1>
			<h1
				class="w-full text-center text-[6vw] tracking-[2rem] whitespace-nowrap text-black/10 lg:text-[5vw]/none"
			>
				RTFOLIOPORTFOLIOPORTFOLIOPORTFOLIOPORTFOLIOPORTFOLIO
			</h1>
			<h1
				class="w-full text-center text-[6vw] tracking-[2rem] whitespace-nowrap text-black/10 lg:text-[5vw]/none"
			>
				RTFOLIOPORTFOLIOPORTFOLIOPORTFOLIOPORTFOLIOPORTFOLIO
			</h1>
			<h1
				class="w-full text-center text-[6vw] tracking-[2rem] whitespace-nowrap text-black/10 lg:text-[5vw]/none"
			>
				RTFOLIOPORTFOLIOPORTFOLIOPORTFOLIOPORTFOLIOPORTFOLIO
			</h1>
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
					href="https://github.com/MainLah"
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
