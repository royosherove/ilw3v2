<script>
	import { each } from 'svelte/internal';

	const links = [
		{ name: 'Discord', url: 'https://discord.gg/YnpgKfcyyW', image: '' },
		{ name: 'Telegram', url: 'https://discord.gg/YnpgKfcyyW', image: '' },
		{ name: 'Meetup', url: 'https://discord.gg/YnpgKfcyyW', image: '' },
		{ name: 'YouTube', url: 'https://discord.gg/YnpgKfcyyW', image: '' },
		{ name: 'Github', url: 'https://discord.gg/YnpgKfcyyW', image: '' }
	];
</script>

<div class="text-white m-auto md:w-1/3 flex-col flex text-center">
	{#each links as link}
		<a href={link.url}>
			<div class="border-white border rounded p-2 underline">{link.name}</div>
		</a>
	{/each}

    <div class="mt-10 text-xl">Live Stream:</div>
    <div style="padding:56.25% 0 0 0;position:relative;" class="mt-1 ">
        <iframe id="r-embed-player-iframe" class="rounded" 
        src="https://player.restream.io/?token=c2b08d5f97664a3dbb1378ceba801a1e" 
        allow="autoplay" allowfullscreen frameborder="0" 
        title="Web3 Israel Stream"
        style="position:absolute;top:0;left:0;width:100%;height:100%;">
    </iframe></div> 
</div>
