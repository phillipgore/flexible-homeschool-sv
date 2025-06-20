<script>
    import tutorialData from "$lib/data/tutorials.json";
    import {base} from '$app/paths';
	import {slide} from 'svelte/transition';
    import {page} from '$app/state';
    import { onMount } from 'svelte';
	import { get } from "svelte/store";

	let { windowWidth } = $props();
	let visible = $state(false);
	let btnNavSlide = $state('');

    const resetMenu = () => {
        btnNavSlide.classList.remove('open');
        visible = false;
    }

	const windowResize = () => {
		if (windowWidth > 767) {
			resetMenu();
		}
	}

	const toggleMenu = () => {
		btnNavSlide.classList.toggle('open');
		visible = !visible
	}

    const tutorialSelected = () => {
        resetMenu();
        getTutorial();
    }

    const getTutorial = () => {
        return tutorialData.find(tut => tut._slug === page.params.slug);
    }

    onMount(() => {
		getTutorial();
	});
</script>

<svelte:window on:resize={() => windowResize()} bind:outerWidth={windowWidth}/>

<!-- Splash -->
<!-- <div class="splash splash-support">
    <div class="container-lg p-tn-v-36">
        <div class="row txt-tn-center p-tn-v-36 p-sm-v-54">
            <h1 class="fnt-size-tn-24 fnt-size-xs-36 fnt-size-sm-46 fnt-size-md-62 cl-white txt-tn-center txt-shadow p-tn-h-9 m-tn-0">Flexible Homeschool <span class="txt-condensed-black cl-success">Tutorials</span></h1>
            <h2 class="fnt-size-tn-16 fnt-size-sm-20 fnt-size-md-24 cl-white txt-tn-center txt-shadow m-tn-b-15">Get a handle on how it all works.</h2>
        </div>
    </div>
</div> -->
<!-- /Splash -->
 
<!-- Content -->
<div class="p-tn-h-9 p-xs-h-18 p-lg-h-0 container-lg m-tn-b-54 m-tn-t-36 m-md-t-54">
    <div class="row">
        <!-- Sidebar -->
        <asside class="col-md-1of3 col-lg-1of4 m-tn-b-36 p-tn-b-36 m-md-b-0 p-md-b-0 dis-tn-none dis-md-block">
            <div class="m-md-r-18 m-lg-r-36">	
                <h1 class="cl-success m-tn-0">Tutorials</h1>
                <h2 class="cl-gray-darker m-tn-t-0 m-tn-b-9">Getting Started</h2>
                {#each tutorialData as tutorial}
                    {#if tutorial.getting_started}
                        <p class="m-tn-b-18">
                            {#if tutorial.has_video}
                                <i class="cl-gray-darkest fss-video m-tn-r-3"></i>
                            {:else}
                                <i class="cl-gray-darkest fss-invoices m-tn-r-3"></i>
                            {/if}
                            <a class="cl-success" href="{base}/tutorials/{tutorial._slug}" onclick={() => getTutorial()}>{ tutorial.title }</a>
                        </p>
                    {/if}
                {/each}
                
                <h2 class="cl-gray-darker p-tn-t-18 m-tn-t-0 m-tn-b-9">Basic Usage</h2>
                {#each tutorialData as tutorial}
                    {#if !tutorial.getting_started}
                        <p class="m-tn-b-18">
                            {#if tutorial.has_video}
                                <i class="cl-gray-darkest fss-video m-tn-r-3"></i>
                            {:else}
                                <i class="cl-gray-darkest fss-invoices m-tn-r-3"></i>
                            {/if}
                            <a class="cl-success" href="{base}/tutorials/{tutorial._slug}" onclick={() => getTutorial()}>{ tutorial.title }</a>
                        </p>
                    {/if}
                {/each}
                
                <a class="btn bg-success txt-tn-center m-tn-t-36" href="mailto:support@aflexiblehomeschool.com">Email Support</a>
            </div>
        </asside>
        <!-- /Sidebar -->

        <!-- Dropdown Nav -->
        <asside class="dis-md-none">
            <div class="clearfix txt-tn-center pos-rel p-tn-tb-7 m-tn-b-18">
                <a bind:this={btnNavSlide} onclick={() => toggleMenu()} aria-label="Navigation Reveal" class="js-btn-tutorial-slide btn-tutorial-slide dis-tn-block fl-tn-left" href="#">
                    <div class="icn-tutorial-slide">
                        <span></span>
                    </div>
                </a>
                <div class="cl-gray-darkest fl-tn-left p-tn-l-45 p-tn-t-2 m-tn-t-neg-18">
                    <i class="fss-caret-left"></i> Click for tutorial list.
                </div>
            </div>
            {#if visible}
                <div class="js-drop-tutorial-nav dis-tn-block dis-md-none" transition:slide="{{duration: 300}}">
                    <h2 class="cl-gray-darker m-tn-t-0 m-tn-b-9">Getting Started</h2>
                    {#each tutorialData as tutorial}
                        {#if tutorial.getting_started}
                            <p class="m-tn-b-18">
                                {#if tutorial.has_video}
                                    <i class="cl-gray-darkest fss-video m-tn-r-3"></i>
                                {:else}
                                    <i class="cl-gray-darkest fss-invoices m-tn-r-3"></i>
                                {/if}
                                <a class="cl-success" href="{base}/tutorials/{tutorial._slug}" onclick={() => tutorialSelected()}>{ tutorial.title }</a>
                            </p>
                        {/if}
                    {/each}
                    <h2 class="cl-gray-darker p-tn-t-18 m-tn-t-0 m-tn-b-9">Basic Usage</h2>
                    {#each tutorialData as tutorial}
                        {#if !tutorial.getting_started}
                            <p class="m-tn-b-18">
                                {#if tutorial.has_video}
                                    <i class="cl-gray-darkest fss-video m-tn-r-3"></i>
                                {:else}
                                    <i class="cl-gray-darkest fss-invoices m-tn-r-3"></i>
                                {/if}
                                <a class="cl-success" href="{base}/tutorials/{tutorial._slug}" onclick={() => tutorialSelected()}>{ tutorial.title }</a>
                            </p>
                        {/if}
                    {/each}
                </div>
            {/if}
        </asside>
        <!-- /Dropdown Nav -->

        <!-- Main -->
        <article class="divider-left col-md-2of3 col-lg-3of4 m-md-t-0 p-md-t-0">
            <div class="m-tn-t-18 m-md-t-0 m-md-l-18 m-lg-l-36">
                {#if page.params.slug}
                    <h1 class="cl-success m-tn-0">{getTutorial().title}</h1>
                    <h2 class="cl-gray-darker m-tn-t-0 m-tn-b-9">{getTutorial().subtitle}</h2>
                    {@html getTutorial().content}
                {:else}
                    <div class="txt-tn-center txt-md-left">
                        <h3 class="cl-success ln-height-125 fnt-size-tn-26 fnt-size-xs-30 fnt-size-sm-36 fnt-size-md-45">
                            Flexible Homeschool <br class="dis-tn-none dis-xs-inline dis-xl-none">Tutorials
                        </h3>
                        <p class="cl-gray-darkest ln-height-150 fnt-size-tn-16 fnt-size-sm-20 fnt-size-md-28">
                            Get a handle on how it all works.
                        </p>
                    </div>
                {/if}
            </div>
        </article>
        <!-- /Main -->
         
        <div class="txt-tn-center">
            <a class="dis-md-none btn bg-success txt-tn-center m-tn-t-36" href="mailto:support@aflexiblehomeschool.com">Email Support</a>
        </div>
    </div>
</div>
<!-- /Content -->