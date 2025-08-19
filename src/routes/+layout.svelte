<script lang="ts">
	import '../app.css';
	import favicon from '$lib/assets/hicon.jpg';
	import { injectAnalytics } from '@vercel/analytics/sveltekit'

	injectAnalytics();
	
	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
</svelte:head>

{@render children?.()}
