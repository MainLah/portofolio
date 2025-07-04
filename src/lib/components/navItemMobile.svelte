<script>
	const { text, href, className } = $props();
</script>

<li class={['bg-lime-950 px-4 py-2 text-lg hover:bg-lime-900', className]}>
	<a {href}>{text}</a>
</li>
