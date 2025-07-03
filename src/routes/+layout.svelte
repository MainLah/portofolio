<script lang="ts">
	import '../app.css';
	import NavItem from '$lib/components/navItem.svelte';

	let { children } = $props();

	const navItems = [
		{ text: 'Home', href: '#home' },
		{ text: 'About', href: '#about' },
		{ text: 'Experience', href: '#experience' },
		{ text: 'Projects', href: '#projects' },
		{ text: 'Contacts', href: '#contacts' }
	];

	let showNavbar = $state(false);

	function handleScroll() {
		const homeSection = document.getElementById('home');
		if (homeSection) {
			const rect = homeSection.getBoundingClientRect();
			showNavbar = rect.bottom <= 0;
		}
	}
</script>

<svelte:window onscroll={handleScroll} />

<div
	class={[
		'fixed inset-x-0 top-8 z-50 flex h-[10vh] w-screen items-center justify-center opacity-0',
		{ 'opacity-100': showNavbar }
	]}
>
	<nav class="max-w-screen-lg">
		<ul class="flex items-center justify-center gap-4 text-amber-200">
			{#each navItems as item}
				<NavItem text={item.text} href={item.href} />
			{/each}
		</ul>
	</nav>
</div>

{@render children()}
