<script>
	import { goto } from '$app/navigation';
	import { onMount } from 'svelte';
	import { WEBUI_BASE_PATH } from '$lib/constants';

	onMount(async () => {
		await goto(WEBUI_BASE_PATH + '/admin/users/overview');
	});
</script>
