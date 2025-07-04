<script lang="ts">
	type Project = {
		year: string;
		name: string;
		description: string;
		href: string;
		className?: string;
	};

	const { year, name, description, href, className }: Project = $props();
</script>

<div
	class={[
		'grid w-2/3 grid-cols-[100px_1fr_auto] items-center gap-8 border-t border-amber-200 px-8 py-12 ',
		className
	]}
>
	<div>
		<p class="text-2xl text-amber-200">{year}</p>
	</div>
	<div class="max-w-screen-sm">
		<h1 class="pb-4 text-2xl text-amber-200">{name}</h1>
		<p class="text-amber-200">
			{description}
		</p>
	</div>
	<div>
		<a
			{href}
			class="inline rounded-[2rem] border border-amber-200 px-6 py-3 text-lg text-amber-200 hover:bg-lime-900"
		>
			View
		</a>
	</div>
</div>
