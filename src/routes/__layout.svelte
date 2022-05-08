<script>
	import '../app.css';
	import { MetaTags } from 'svelte-meta-tags';
</script>

<head>
	<MetaTags
		title="קהילת פיתוח ווב3 בישראל"
		titleTemplate="קהילת פיתוח ווב3 בישראל"
		description="דף הבית של קהילת פיתוח ווב3 בישראל - מפגשים דיסקורד טלגרם ועוד"
		canonical="https://www.israelweb3.com"
		openGraph={{
			url: 'https://www.israelweb3.com',
			title: 'Afikoman 2022 Israel web3',
			description: 'הגרלת האפיקומן של ווב3',
			images: [
				{
					url: 'https://www.israelweb3.com/bored.png',
					width: 800,
					height: 600,
					alt: 'Israel Web3'
				}
			],
			site_name: 'קהילת פיתוח ווב3 בישראל'
		}}
	/>
</head>

<div class="mt-10 md:mt-20">
	<slot />
</div>
