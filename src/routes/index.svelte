<script>
	import { each } from 'svelte/internal';

	const links = [
		{ name: 'דיסקורד (פיתוחי)', url: 'https://discord.gg/YnpgKfcyyW', image: 'discord.png' },
		{ name: 'טלגרם', url: 'https://t.me/+-sEflgfrqDoyYWVk', image: 'telegram.png' },
		{ name: 'מיטאפים', url: 'https://www.meetup.com/ilw3-israel-web-3-0-smart-contracts-dev-meetup/', image: 'meetup.png' },
		{ name: 'YouTube', url: 'https://youtube.com/channel/UCRfgLdabcXDFKhv_BFazjYw', image: 'youtube.png' },
	];
	const otherLinks = [
		{ name: 'Web3il (לא פיתוחי)', url: 'https://discord.gg/2qTfa2HKWn', image: 'discord.png' },
		{ name: 'קהילת פייסבוק', url: 'https://www.facebook.com/groups/web3.israel', image: 'fb.png' },
	];
</script>

<div class="m-auto md:w-1/3 flex-col flex text-center space-y-2">
    <img src='bored.png' alt='logo'   width="200" height="200" class='rounded-full m-auto ' />
    <div class="text-white font-mono">קהילת פיתוח ווב3 בישראל</div>
	{#each links as link}
		<a href={link.url} class="">
			<div class="border-black w-3/4 md:w-2/4  m-auto bg-gray-50 border rounded p-2 flex items-center ">
                <img alt='icon' src={link.image} class="w-7 mr-4 ml-14 "/>
                <div>
                    {link.name}
                </div>
			</div>
		</a>
	{/each}
    <div class="text-white font-mono mt-10">לינקים נוספים</div>
	{#each otherLinks as link}
		<a href={link.url} class="">
			<div class="border-black w-3/4  md:w-2/4 m-auto bg-gray-50 border rounded p-2 flex items-center ">
                <img alt='icon' src={link.image} class="w-7 mr-4 ml-14"/>
                <div>
                    {link.name}
                </div>
			</div>
		</a>
	{/each}

	<div class="mt-10 text-xl text-white">Live Stream:</div>
	<div style="padding:56.25% 0 0 0;position:relative;" class="mt-1 mx-2 ">
		<iframe
			id="r-embed-player-iframe"
			class="rounded"
			src="https://player.restream.io/?token=c2b08d5f97664a3dbb1378ceba801a1e"
			allow="autoplay"
			allowfullscreen
			frameborder="0"
			title="Web3 Israel Stream"
			style="position:absolute;top:0;left:0;width:100%;height:100%;"
		/>
	</div>
</div>
