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
</script>

<div class="absolute inset-x-0 top-8 z-50 flex h-[10vh] w-screen items-center justify-center">
	<nav class="max-w-screen-lg rounded-4xl border border-zinc-300 bg-white px-8 py-3 shadow-lg">
		<ul class="flex items-center justify-center gap-4">
			{#each navItems as item}
				<NavItem text={item.text} href={item.href} />
			{/each}
		</ul>
	</nav>
</div>

{@render children()}
