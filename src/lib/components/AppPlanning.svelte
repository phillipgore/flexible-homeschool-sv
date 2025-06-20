<script>
    import desktopPlanning3 from '$lib/assets/desktop-planning-3.png';
    import laptopPlanning3 from '$lib/assets/laptop-planning-3.png';
    import tabletPlanning3 from '$lib/assets/tablet-planning-3.png';
    import phonePlanning3 from '$lib/assets/phone-planning-3.png';

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

<!-- Flexible Planning -->
<div class="container-lg p-tn-h-9 p-xs-h-18 p-tn-v-36 p-md-v-72 p-lg-h-0">
	<div class="row m-tn-b-27">
		<div class="col-md-1of2 js-switch-container switch-container p-md-t-72 p-lg-t-0">
			<img alt="Desktop" class="switch-item img-tn-flex m-tn-b-54 {isActive.desktop ? 'active' : 'dis-tn-none'}" src="{desktopPlanning3}" />
			<img alt="Laptop" class="switch-item img-tn-flex m-tn-b-54 {isActive.laptop ? 'active' : 'dis-tn-none'}" src="{laptopPlanning3}" />
			<img alt="Tablet" class="switch-item img-tn-flex m-tn-b-54 {isActive.tablet ? 'active' : 'dis-tn-none'}" src="{tabletPlanning3}" />
			<img alt="Phone" class="switch-item img-tn-flex m-tn-b-54 {isActive.phone ? 'active' : 'dis-tn-none'}" src="{phonePlanning3}" />
			<div class="btn-pill-collection txt-tn-center">
				<button onclick={() => switchImage('desktop')} class="switch-btn first {isActive.desktop ? 'active' : ''}">Desktop</button>
				<button onclick={() => switchImage('laptop')} class="switch-btn {isActive.laptop ? 'active' : ''}">Laptop</button>
				<button onclick={() => switchImage('tablet')} class="switch-btn {isActive.tablet ? 'active' : ''}">Tablet</button>
				<button onclick={() => switchImage('phone')} class="switch-btn last {isActive.phone ? 'active' : ''}">Phone</button>
			</div>
		</div>
		<div class="col-md-1of2 p-tn-t-54 p-md-t-0 p-md-l-18 p-lg-l-36">
			<div class="row m-tn-b-18">
				<div class="icn-circle fl-tn-left m-tn-r-18">
					<i class="fss-planning"></i>
				</div>
				<h2 class="font-weight-400 line-height-1 p-tn-t-9 m-tn-0">Flexible <span class="txt-condensed-black cl-success">Planning</span></h2>
				<h3 class="font-weight-400 cl-gray-darkest m-tn-0">Plans that work with your life,<br class="dis-tn-none dis-xs-inline dis-lg-none"> not against it.</h3>
			</div>
			<div class="m-md-l-27">
				<h4>Timeframes</h4>
				<p>Plan your school year by flexible terms and weeks per term, not rigid dates on a calendar that tend to come undone once real life begins to happen.</p>
				<h4>Resources</h4>
				<p>Maintain a list of resources (books, links, videos, audio, apps) for your homeschool. Attach resources to school work for later reference and your records.</p>
				<h4>Individualized</h4>
				<p class="m-tn-b-0">Plan school work around the individual needs and pace of each child. Speed up or slow down––our system can handle it with no extra effort on your part.</p>
			</div>
		</div>
	</div>
</div>
<!-- Flexible Planning -->