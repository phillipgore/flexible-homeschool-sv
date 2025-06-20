<script>
	import AppComparison from "$lib/components/AppComparison.svelte";
	import AppPlanning from "$lib/components/AppPlanning.svelte";
	import AppProgressSplash from "$lib/components/AppProgressSplash.svelte";
	import AppReporting from "$lib/components/AppReporting.svelte";
	import AppRigidSplash from "$lib/components/AppRigidSplash.svelte";
	import AppSplash from "$lib/components/AppSplash.svelte";
	import AppTracking from "$lib/components/AppTracking.svelte";
</script>

<AppSplash></AppSplash>
<AppPlanning></AppPlanning>
<div class="bg-gray-lightest">
    <AppTracking></AppTracking>
</div>
<AppReporting></AppReporting>
<div class="bg-gray-lightest">
    <AppComparison></AppComparison>
</div>
