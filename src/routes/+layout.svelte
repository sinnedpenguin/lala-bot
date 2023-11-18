<script>
	import { onNavigate } from '$app/navigation';
	import { onMount } from "svelte";
	import SiteHeader from '$lib/components/site-header.svelte';
	import SiteFooter from '$lib/components/site-footer.svelte';
	import { ModeWatcher, setMode } from "mode-watcher";
	import '../app.postcss';

	onNavigate((navigation) => {
		// eslint-disable-next-line @typescript-eslint/ban-ts-comment
		// @ts-ignore
		if (!document.startViewTransition) return;

		return new Promise((resolve) => {
			// eslint-disable-next-line @typescript-eslint/ban-ts-comment
			// @ts-ignore
			document.startViewTransition(async () => {
				resolve();
				await navigation.complete;
			});
		});
	});

	onMount(() => {
    setMode("dark");
  });
</script>

<ModeWatcher />
<SiteHeader />
<slot />
<SiteFooter />