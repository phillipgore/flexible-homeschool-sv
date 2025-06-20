<script>
    import {base} from '$app/paths';
	import {slide} from 'svelte/transition';

	let { windowWidth } = $props();
	let visible = $state(false);
	let btnNavSlide;

	const windowResize = () => {
		if (windowWidth > 767) {
			btnNavSlide.classList.remove('open');
			visible = false;
		}
	}

	const toggleMenu = () => {
		btnNavSlide.classList.toggle('open');
		visible = !visible
	}
</script>

<svelte:window on:resize={() => windowResize()} bind:outerWidth={windowWidth}/>

<!-- Header -->
<header>
	<div class="container-lg">
		<div class="row p-sm-r-12 p-lg-r-0 p-xl-h-0 m-xl-r-neg-6">
			<div class="col-tn-7of9 col-sm-5of12 p-tn-l-9 p-xs-l-18 p-lg-l-0">
				<a class="logo" href="{base}/home">
					<i class="fss-logo"></i> <span class=""> Flexible Homeschool</span>
				</a>
			</div>
			<nav class="dis-tn-none dis-md-block | col-tn-2of9 col-sm-7of12 txt-tn-right">
				<ul>
					<li><a href="{base}/">Home</a></li>
					<li><a href="{base}/application">App</a></li>
					<li><a href="/#price">Price</a></li>
                    <li><a href="{base}/tutorials">Tuts</a></li>
                    <li><a href="{base}/faq">FAQ</a></li>
					<!-- <li><a href="{base}/new">New</a></li> -->
					<li>
						<a target="_blank" href="https://app.aflexiblehomeschool.com/sign-in" class="m-tn-r-6 m-xs-r-12 m-sm-r-0">
							Sign In
						</a>
					</li>
					<span class="cl-white m-tn-l-3">|</span>
					<li>
						<a target="_blank" href="https://app.aflexiblehomeschool.com/" class="m-tn-r-6 m-xs-r-12 m-sm-r-0">
							Sign Up
						</a>
					</li>
				</ul>
			</nav>
			<a bind:this={btnNavSlide} onclick={() => toggleMenu()} class="btn-nav-slide dis-tn-block dis-md-none" href="#" aria-label="Navigation Reveal">
				<div class="icn-nav-slide">
					<span></span>
				</div>
			</a>
		</div>
	</div>
</header>
<!-- /Header -->

<!-- Drop Nav -->
 {#if visible}
	<nav class="drop-nav dis-tn-block dis-md-none" transition:slide="{{duration: 300}}">
		<ul>
			<li><a href="{base}/">Home</a></li>
			<li><a href="{base}/application">App</a></li>
			<li><a href="/#price">Price</a></li>
			<li><a href="{base}/tutorials">Tuts</a></li>
			<li><a href="{base}/faq">FAQ</a></li>
			<!-- <li><a href="{base}/new">New</a></li> -->
			<li>
				<a target="_blank" href="https://app.aflexiblehomeschool.com/sign-in" class="m-tn-r-6 m-xs-r-12 m-sm-r-0">
					Sign In
				</a>
			</li>
			<li>
				<a target="_blank" href="https://app.aflexiblehomeschool.com" class="m-tn-r-6 m-xs-r-12 m-sm-r-0">
					Sign Up
				</a>
			</li>
		</ul>
	</nav>
{/if}
<!-- /Drop Nav -->

<!-- Sub Header -->
<div class="sub-header"></div>
<!-- /Sub Header -->