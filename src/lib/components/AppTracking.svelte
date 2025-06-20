<script>
    import desktopTracking3 from '$lib/assets/desktop-tracking-3.png';
    import laptopTracking3 from '$lib/assets/laptop-tracking-3.png';
    import tabletTracking3 from '$lib/assets/tablet-tracking-3.png';
    import phoneTracking3 from '$lib/assets/phone-tracking-3.png';

	let isActive = {
		desktop: false,
		laptop: true,
		tablet: false,
		phone: false,
	}

	const switchImage = (device) => {
		Object.keys(isActive).forEach(key => {
			isActive[key] = false;
		});
		isActive[device] = true;
	}
</script>

<!-- Flexible Tracking -->
<div class="container-lg p-tn-h-9 p-xs-h-18 p-tn-v-36 p-md-v-72 p-lg-h-0">
	<div class="row m-tn-b-27">
		<div class="col-md-1of2 js-switch-container switch-container fl-md-right p-md-t-72 p-lg-t-45">
			<img alt="Desktop" class="switch-item img-tn-flex m-tn-b-54 {isActive.desktop ? 'active' : 'dis-tn-none'}" src="{desktopTracking3}" />
			<img alt="Laptop" class="switch-item img-tn-flex m-tn-b-54 {isActive.laptop ? 'active' : 'dis-tn-none'}" src="{laptopTracking3}" />
			<img alt="Tablet" class="switch-item img-tn-flex m-tn-b-54 {isActive.tablet ? 'active' : 'dis-tn-none'}" src="{tabletTracking3}" />
			<img alt="Phone" class="switch-item img-tn-flex m-tn-b-54 {isActive.phone ? 'active' : 'dis-tn-none'}" src="{phoneTracking3}" />
			<div class="btn-pill-collection txt-tn-center">
				<button onclick={() => switchImage('desktop')} class="switch-btn first {isActive.desktop ? 'active' : ''}">Desktop</button>
				<button onclick={() => switchImage('laptop')} class="switch-btn {isActive.laptop ? 'active' : ''}">Laptop</button>
				<button onclick={() => switchImage('tablet')} class="switch-btn {isActive.tablet ? 'active' : ''}">Tablet</button>
				<button onclick={() => switchImage('phone')} class="switch-btn last {isActive.phone ? 'active' : ''}">Phone</button>
			</div>
		</div>
		<div class="col-md-1of2 fl-md-left p-tn-t-54 p-md-t-0 p-md-r-18 p-lg-r-36">
			<div class="row m-tn-b-18">
				<div class="icn-circle fl-tn-left m-tn-r-18">
					<i class="fss-tracking"></i>
				</div>
				<h2 class="font-weight-400 line-height-1 p-tn-t-9 m-tn-0">Flexible <span class="txt-condensed-black cl-success">Tracking</span></h2>
				<h3 class="font-weight-400 cl-gray-darkest m-tn-0">Know what's done and what's left to do.</h3>
			</div>
			<div class="m-md-l-27">
				<h4>Set Your Pace</h4>
				<p>One child goes faster with math. Another goes a little slower with reading. Flexible Homeschool App can handle it. Even if you must stop school for a couple of days, simply pick back up right where you left off.</p>
				<p>No alerts screaming that you’re falling behind and no piling up supposedly overdue work. Move through school work at the proper pace for each child.</p>
				<h4>Track Your Progress</h4>
				<p>Flexible Homeschool App is about recording what you actually did, when you did it and how long it took you to do it. It keeps pace with your child. It does not demand that your child keep pace with it.</p>
				<p class="m-tn-b-0">Progress bars show each child’s advancement, giving you a quick sense of how many of the planned lesson times you have completed and how many you have yet to complete.</p>
			</div>
		</div>
	</div>
</div>
<!-- Flexible Tracking -->