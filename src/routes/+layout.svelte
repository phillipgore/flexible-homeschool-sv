<script>
	import Header from '$lib/components/Header.svelte';
	import Footer from '$lib/components/Footer.svelte';
	import '$lib/stylesheets/flexible-styles.css';
</script>

<svelte:head>
	<title>Flexible Homeschool App</title>
</svelte:head>

<Header></Header>
<div class="wrapper">
	<slot/>
</div>
<Footer></Footer>