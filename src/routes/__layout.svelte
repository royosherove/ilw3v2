<script>
	import '../app.css';
	import { MetaTags } from 'svelte-meta-tags';
	import Footer from '../components/Footer.svelte';
	import NavBar from '../components/NavBar.svelte';
</script>

<svelte:head>
	<script async src="//static.getclicky.com/101367315.js"></script>
	<noscript
		><p>
			<img alt="Clicky" width="1" height="1" src="//in.getclicky.com/101367315ns.gif" />
		</p></noscript
	>

	<MetaTags
		title="קהילת ווב3 בישראל"
		titleTemplate="קהילת ווב3 בישראל"
		description="דף הבית של קהילת ווב3 בישראל - מפגשים דיסקורד טלגרם ועוד"
		canonical="https://www.israelweb3.com"
		openGraph={{
			url: 'https://www.israelweb3.com',
			title: 'קהילת ווב3 בישראל',
			description: 'קהילת ווב3 בישראל',
			images: [
				{
					url: 'https://www.israelweb3.com/bored.png',
					width: 800,
					height: 600,
					alt: 'Israel Web3'
				}
			],
			site_name: 'קהילת ווב3 בישראל'
		}}
	/>
</svelte:head>
<div class="">
	<NavBar />
	<div class="m-auto text-center p-2">
		<img src="bored.png" alt="logo" width="200" height="200" class="rounded-full m-auto " />
		<div class="text-white font-mono">קהילת ווב3 בישראל</div>
	</div>
	<slot />
	<Footer />
</div>
