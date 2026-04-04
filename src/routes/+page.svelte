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

<!-- Contact Info -->
<div class="container-md m-tn-b-72 m-tn-t-36 m-md-t-54">
    <div class="row m-tn-b-72 p-tn-rl-9 p-tn-b-72 p-xs-rl-18">
        <!-- <h1 class="h1-lg txt-tn-center m-tn-b-15">Thank you to everyone who used the app. If you need help, support will be minimal but we will do what we can.</h1> -->
        <div class="p-tn-b-72 p-md-r-36">
            <div class="txt-tn-center m-tn-tb-36">
                <div class="m-tn-b-27"><i class="fss-support cl-gray-dark fnt-size-tn-80"></i></div>
                <a class="btn bg-success txt-tn-center" href="mailto:support@aflexiblehomeschool.com">Support Email</a>
            </div>
            <p class="txt-tn-justify">
                Click the button above to email support for help if you are having a problem with the app. Please make sure you check the <a class="cl-success" href="{base}/tutorials">tutorials</a> first.
            </p>
        </div>
    </div>
</div>
<!-- /Contact Info -->