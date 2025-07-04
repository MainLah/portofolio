<script lang="ts">
	import '../app.css';
	import NavItem from '$lib/components/navItem.svelte';

	let { children } = $props();

	const navItems = [
		{ text: 'Home', href: '#home' },
		{ text: 'About', href: '#about' },
		{ text: 'Projects', href: '#projects' },
		{ text: 'Contacts', href: '#contacts' }
	];

	let showNavbar = $state(false);

	function handleScroll() {
		const homeSection = document.getElementById('home');
		const contactSection = document.getElementById('contacts');
		if (homeSection && contactSection) {
			const rect1 = homeSection.getBoundingClientRect();
			const rect2 = contactSection.getBoundingClientRect();
			showNavbar = rect1.bottom <= 0 && rect2.top >= 0;
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
