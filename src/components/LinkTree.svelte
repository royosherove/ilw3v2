<script>
	// import EventsCalendar from '../src/components/eventsCalendar.svelte';
	import { each } from 'svelte/internal';

	const links = [
		{ name: 'דיסקורד (פיתוחי)', url: 'https://discord.gg/YnpgKfcyyW', image: 'discord.png' },
		{ name: 'טלגרם (פיתוחי)', url: 'https://t.me/+-sEflgfrqDoyYWVk', image: 'telegram.png' },
		{ name: 'מיטאפ (פיתוחי)', url: 'https://www.meetup.com/ilw3-israel-web-3-0-smart-contracts-dev-meetup/', image: 'meetup.png' },
		{ name: 'YouTube (פיתוחי)', url: 'https://youtube.com/channel/UCRfgLdabcXDFKhv_BFazjYw', image: 'youtube.png' },
		{ name: 'ווב3 בפייסבוק (פיתוחי)', url: 'https://www.facebook.com/groups/web3.israel', image: 'fb.png' },
		{ name: 'מטא בילדרס (פיתוחי)', url: 'https://www.facebook.com/groups/metabuilders', image: 'fb.png' },
	];
	const otherLinks = [
		{ name: 'Web3il (כללי)', url: 'https://discord.gg/2qTfa2HKWn', image: 'discord.png' },
	];
</script>

<div class="text-white font-mono mt-10">לינקים בנושא פיתוח</div>
{#each links as link}
	<a href={link.url} class="">
		<div
			class="border-black w-3/4 md:w-2/4  m-auto bg-gray-50 border rounded p-2 flex items-center "
		>
			<img alt="icon" src={link.image} class="w-7 mr-4 ml-14 " />
			<div>
				{link.name}
			</div>
		</div>
	</a>
{/each}
<div class="text-white font-mono mt-10">לינקים נוספים</div>
{#each otherLinks as link}
	<a href={link.url} class="">
		<div
			class="border-black w-3/4  md:w-2/4 m-auto bg-gray-50 border rounded p-2 flex items-center "
		>
			<img alt="icon" src={link.image} class="w-7 mr-4 ml-14" />
			<div>
				{link.name}
			</div>
		</div>
	</a>
{/each}
