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
		'group grid w-full grid-cols-1 items-center gap-8 border-t border-amber-200 px-4 py-8 hover:bg-amber-200 md:w-2/3 md:grid-cols-[100px_1fr_auto] md:px-8 md:py-12 ',
		className
	]}
>
	<div class="md:row-auto">
		<p class="text-2xl text-amber-200 group-hover:text-lime-950">{year}</p>
	</div>
	<div class="nd:row-auto max-w-screen-sm">
		<h1 class="pb-4 text-2xl text-amber-200 group-hover:text-lime-950">{name}</h1>
		<p class="text-amber-200 group-hover:text-lime-950">
			{description}
		</p>
	</div>
	<div>
		<a
			{href}
			class="col-span-full mt-4 flex rounded-[2rem] border border-amber-200 px-6 py-3 text-lg text-amber-200 group-hover:bg-lime-950 group-hover:text-amber-200 hover:bg-lime-900 md:col-auto md:row-auto md:mt-0 md:justify-end"
		>
			View
		</a>
	</div>
</div>
