<script>
	import { ModeWatcher } from "mode-watcher";
	import SiteHeader from '$lib/components/site-header.svelte';
	import SiteFooter from '$lib/components/site-footer.svelte';
	import '../app.postcss';

	import { onNavigate } from '$app/navigation';

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
</script>

<ModeWatcher />
<SiteHeader />
<slot />
<SiteFooter />