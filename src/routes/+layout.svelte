<script lang="ts">
	import '../app.css';
	import NavItem from '$lib/components/navItem.svelte';
	import NavItemMobile from '$lib/components/navItemMobile.svelte';

	let { children } = $props();

	type NavItems = {
		text: string;
		href: string;
	};

	const navItems = [
		{ text: 'Home', href: '#home' },
		{ text: 'About', href: '#about' },
		{ text: 'Projects', href: '#projects' },
		{ text: 'Contacts', href: '#contacts' }
	];

	let showNavbar = $state(false);
	let mobileOpenNavbar = $state(false);

	function handleScroll() {
		const homeSection = document.getElementById('home');
		const contactSection = document.getElementById('contacts');
		if (homeSection && contactSection) {
			const rect1 = homeSection.getBoundingClientRect();
			const rect2 = contactSection.getBoundingClientRect();
			showNavbar = rect1.bottom <= 0 && rect2.top >= 0;
		}
	}

	function checkOrderOfNavItems(navItems: NavItems[], i: number) {
		if (i === 0) {
			return 'rounded-t-lg';
		} else if (i === navItems.length - 1) {
			return 'rounded-b-lg';
		}
	}
</script>

<svelte:window onscroll={handleScroll} />

<div
	class={[
		'fixed inset-x-0 top-4 z-50 flex h-[10vh] w-screen items-center justify-center opacity-0 md:top-8',
		{ 'opacity-100': showNavbar }
	]}
>
	<nav class="hidden max-w-screen-lg md:block">
		<ul class="flex items-center justify-center gap-4 text-amber-200">
			{#each navItems as item}
				<NavItem text={item.text} href={item.href} />
			{/each}
		</ul>
	</nav>
	<nav class="block max-w-screen-lg md:hidden">
		<ul class="relative flex items-center justify-center gap-4 text-amber-200">
			<button
				aria-label="open"
				class="rounded-lg border border-amber-200 bg-lime-950 p-1"
				onclick={() => (mobileOpenNavbar = !mobileOpenNavbar)}
			>
				<svg
					xmlns="http://www.w3.org/2000/svg"
					width="24"
					height="24"
					viewBox="0 0 24 24"
					fill="none"
					stroke="currentColor"
					stroke-width="2"
					stroke-linecap="round"
					stroke-linejoin="round"
					class="lucide lucide-menu-icon lucide-menu"
					><path d="M4 12h16" /><path d="M4 18h16" /><path d="M4 6h16" /></svg
				>
			</button>
			{#if mobileOpenNavbar}
				<div class="absolute top-10 rounded-lg border border-amber-200">
					{#each navItems as item, i}
						<NavItemMobile
							text={item.text}
							href={item.href}
							className={checkOrderOfNavItems(navItems, i)}
						/>
					{/each}
				</div>
			{/if}
		</ul>
	</nav>
</div>

{@render children()}
