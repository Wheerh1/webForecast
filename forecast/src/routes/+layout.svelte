<script>
	import favicon from '$lib/assets/favicon.svg';
	let isDark = false;
	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
	<link rel="stylesheet" href={isDark ? "$lib/styleDark.css" : "$lib/styleLight.css"}/>
</svelte:head>


{@render children?.()}




