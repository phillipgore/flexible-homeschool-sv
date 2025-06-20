<script>
    let { windowHeight } = $props();
    let ready;
    let unexpected;
    let progress;
    
    const annimationTriger = () => {
        let windowTrigger = windowHeight * 0.66666;

        if (ready) {
            if (windowTrigger > Math.round(ready.getBoundingClientRect().top)) {
                ready.classList.add('animate');
            }
        }

        if (unexpected) {
            if (windowTrigger > Math.round(unexpected.getBoundingClientRect().top)) {
                unexpected.classList.add('animate');
            }
        }

        if (progress) {
            if (windowTrigger > Math.round(progress.getBoundingClientRect().top)) {
                progress.classList.add('animate');
            }
        }
    }
</script>

<svelte:window on:scroll={() => annimationTriger()} bind:innerHeight={windowHeight}/>

<!-- Plan -->
<div class="container-lg p-tn-h-9 p-xs-h-18 p-tn-v-36 p-md-v-72 p-lg-h-0">
	<div class="row m-md-rl-neg-18 m-lg-rl-neg-36">

		<div class="col-tn-1of1 | col-xs-2of3 | col-sm-1of2 off-sm-0 | col-md-1of3 p-md-rl-18 | p-lg-rl-36">
			<div bind:this={ready} id="icn-ready" class="icn-ready m-tn-rl-auto m-tn-b-27 m-md-b-45">
				<div class="check"></div>
			</div>
			<h3 id="ready" class="txt-tn-center">1. Ready for the day.</h3>
			<p class="txt-tn-justify">Set what items of School Work you would like to be accomplished for the day. Provide additional specific instuctions if needed.</p>
		</div>

		<div class="col-tn-1of1 | col-xs-2of3 off-xs-1of6 | col-sm-1of2 off-sm-1of4 | col-md-1of3 off-md-0 p-md-rl-18 | p-lg-rl-36">
			<div bind:this={unexpected} id="icn-unexpected" class="icn-unexpected m-tn-rl-auto m-tn-tb-27 m-md-t-0 m-md-b-45"></div>
			<h3 id="unexpected" class="txt-tn-center">2. Handle the unexpected.</h3>
			<p class="txt-tn-justify">Speed up, slow down, even stop when necessary without any extra effort on your part. The app flows arround the unexpected realities of life.</p>
		</div>

		<div class="col-tn-1of1 | col-xs-2of3 off-xs-1of3 | col-sm-1of2 off-sm-1of2 | col-md-1of3 off-md-0 p-md-rl-18 | p-lg-rl-36">
			<div bind:this={progress} id="icn-progress" class="icn-progress m-tn-rl-auto m-tn-tb-27 m-md-t-0 m-md-b-45">
				<div class="meter width-25"></div>
				<div class="meter width-50"></div>
				<div class="meter"></div>
			</div>
			<h3 id="progress" class="txt-tn-center">3. Feel the progress.</h3>
			<p class="txt-tn-justify">See progress unfold before your eyes. Progress meters show you exactly how much you have accomplished for the year, term and week.</p>
		</div>

	</div>
</div>
<!-- Plan -->