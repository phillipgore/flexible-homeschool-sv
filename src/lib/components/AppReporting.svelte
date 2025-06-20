<script>
    import desktopReporting3 from '$lib/assets/desktop-reporting-3.png';
    import laptopReporting3 from '$lib/assets/laptop-reporting-3.png';
    import tabletReporting3 from '$lib/assets/tablet-reporting-3.png';
    import phoneReporting3 from '$lib/assets/phone-reporting-3.png';

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

<!-- Flexible Reporting -->
<div class="container-lg p-tn-h-9 p-xs-h-18 p-tn-v-36 p-md-v-72 p-lg-h-0">
	<div class="row m-tn-b-27">
		<div class="col-md-1of2 js-switch-container switch-container fl-md-right p-md-t-72 p-lg-t-45">
			<img alt="Desktop" class="switch-item img-tn-flex m-tn-b-54 {isActive.desktop ? 'active' : 'dis-tn-none'}" src="{desktopReporting3}" />
			<img alt="Laptop" class="switch-item img-tn-flex m-tn-b-54 {isActive.laptop ? 'active' : 'dis-tn-none'}" src="{laptopReporting3}" />
			<img alt="Tablet" class="switch-item img-tn-flex m-tn-b-54 {isActive.tablet ? 'active' : 'dis-tn-none'}" src="{tabletReporting3}" />
			<img alt="Phone" class="switch-item img-tn-flex m-tn-b-54 {isActive.phone ? 'active' : 'dis-tn-none'}" src="{phoneReporting3}" />
			<div class="btn-pill-collection txt-tn-center">
				<button onclick={() => switchImage('desktop')} class="switch-btn first {isActive.desktop ? 'active' : ''}">Desktop</button>
				<button onclick={() => switchImage('laptop')} class="switch-btn {isActive.laptop ? 'active' : ''}">Laptop</button>
				<button onclick={() => switchImage('tablet')} class="switch-btn {isActive.tablet ? 'active' : ''}">Tablet</button>
				<button onclick={() => switchImage('phone')} class="switch-btn last {isActive.phone ? 'active' : ''}">Phone</button>
			</div>
		</div>
		<div class="col-md-1of2 p-tn-t-54 p-md-t-0 p-lg-t-18 p-md-l-18 p-lg-l-36">
			<div class="row m-tn-b-18">
				<div class="icn-circle fl-tn-left m-tn-r-18">
					<i class="fss-reporting"></i>
				</div>
				<h2 class="font-weight-400 line-height-1 p-tn-t-9 m-tn-0">Flexible <span class="txt-condensed-black cl-success">Reporting</span></h2>
				<h3 class="font-weight-400 cl-gray-darkest m-tn-0">Customizable and printable reports.</h3>
			</div>
			<div class="m-md-l-27">
				<h4 class="m-tn-0">Customizable</h4>
				<p>Create custom reports to reflect a wide variety of data based on what you have recorded (School Year, Terms, School Work, Resources). View the report for any student and any school year.</p>
				<h4 class="m-tn-0">Printable</h4>
				<p class="m-tn-b-0">If you need to include specific reports in your child’s portfolio or if you just love paper and want to print reports, you can. In fact, you can print more than reports. You can print every view in the app.</p>
			</div>
		</div>
	</div>
</div>
<!-- Flexible Reporting -->