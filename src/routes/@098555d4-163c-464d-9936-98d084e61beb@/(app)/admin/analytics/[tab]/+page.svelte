<script>
	import { onMount } from 'svelte';
	import { goto } from '$app/navigation';
	import { config } from '$lib/stores';
	import Analytics from '$lib/components/admin/Analytics.svelte';
	import { WEBUI_BASE_PATH } from '$lib/constants';

	onMount(() => {
		if (!($config?.features.enable_admin_analytics ?? true)) {
			goto(WEBUI_BASE_PATH + '/admin');
		}
	});
</script>

{#if $config?.features.enable_admin_analytics ?? true}
	<Analytics />
{/if}
