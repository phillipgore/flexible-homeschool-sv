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
	import HomeShutdownSplash from "$lib/components/HomeShutdownSplash.svelte";
    import {base} from '$app/paths';
</script>

<!-- <HomeSplash></HomeSplash>
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
</div> -->


<HomeShutdownSplash></HomeShutdownSplash>

<div class="container-lg p-tn-h-9 p-xs-h-18 p-tn-v-36 p-md-v-72 p-lg-h-0">
	<div class="row m-md-rl-neg-18 m-lg-rl-neg-36">

		<div class="col-tn-1of1 | col-xs-2of3 | col-sm-1of2 off-sm-0 | col-md-1of3 p-md-rl-18 | p-lg-rl-36">
			<h3 id="ready" class="txt-tn-center">Need to figure it out?</h3>
			<p class="txt-tn-justify">Refresh yourself on the planning, tracking, reporting and more. Everything from the interface to billing and resetting xsyour password can be found here.</p>
			<a class="btn bg-success txt-tn-center dis-tn-block m-tn-tb-36" href="{base}/tutorials">Tutorials</a>
		</div>

		<div class="col-tn-1of1 | col-xs-2of3 off-xs-1of6 | col-sm-1of2 off-sm-1of4 | col-md-1of3 off-md-0 p-md-rl-18 | p-lg-rl-36">
			<h3 id="unexpected" class="txt-tn-center">Have you got questions?</h3>
			<p class="txt-tn-justify">Over the years we have been asked a lot of different questions. This is a repository of the answers to the questions we have been asked the most.</p>
			<a class="btn bg-success txt-tn-center dis-tn-block m-tn-tb-36" href="{base}/faq">FAQ</a>
		</div>

		<div class="col-tn-1of1 | col-xs-2of3 off-xs-1of3 | col-sm-1of2 off-sm-1of2 | col-md-1of3 off-md-0 p-md-rl-18 | p-lg-rl-36">
			<h3 id="progress" class="txt-tn-center">How can we help?</h3>
			<p class="txt-tn-justify">Click the button below to email support for help if you are having a problem with the app. Please make sure you check the <a class="cl-success" href="{base}/tutorials">tutorials</a> and the <a class="cl-success" href="{base}/faq">FAQ</a> first.</p>
			<a class="btn bg-success txt-tn-center dis-tn-block m-tn-tb-36" href="mailto:fhasupport@icloud.com">Email</a>
		</div>

	</div>
</div>