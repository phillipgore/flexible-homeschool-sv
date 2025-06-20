<script>
	import Footer from "$lib/components/Footer.svelte";
	import Header from "$lib/components/Header.svelte";
	import HomeCredibility from "$lib/components/HomeCredibility.svelte";
	import HomePlan from "$lib/components/HomePlan.svelte";
	import HomePrice from "$lib/components/HomePrice.svelte";
	import HomeQuestions from "$lib/components/HomeQuestions.svelte";
	import HomeSplash from "$lib/components/HomeSplash.svelte";
	import HomeTestimony from "$lib/components/HomeTestimony.svelte";
	import HomeVideo from "$lib/components/HomeVideo.svelte";
</script>

<HomeSplash></HomeSplash>
<HomePlan></HomePlan>

<div class="bg-gray-lightest">
    <HomeVideo></HomeVideo>
</div>

<HomeTestimony></HomeTestimony>

<div class="bg-gray-lightest">
    <HomeQuestions></HomeQuestions>
</div>

<HomeCredibility></HomeCredibility>

<div class="bg-gray-lightest">
    <HomePrice></HomePrice>
</div>
