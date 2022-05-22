<script>
	// import EventsCalendar from '../src/components/eventsCalendar.svelte';
	import { each } from 'svelte/internal';
	import * as allLinks from '../links.json' ;
</script>

<div class="md:flex md:space-x-12 md:m-auto">
	<div>
		<div class="text-white font-mono mt-10">לינקים בנושא פיתוח</div>
		{#each allLinks.devlinks as link}
			<a href={link.url} class="">
				<div
					class="border-black w-3/4 md:w-full my-2 m-auto bg-gray-50 border rounded p-2 md:p-3 flex items-center "
				>
					<img alt="icon" src={link.image} class="w-7 mr-4 ml-14 md:ml-2 md:mr-2 " />
					<div>
						{link.name}
					</div>
				</div>
			</a>
		{/each}
	</div>
	<div>
		<div class="text-white font-mono mt-10">לינקים כלליים</div>
		{#each allLinks.generalLinks as link}
			<a href={link.url} class="">
				<div
					class="border-black w-3/4 md:w-full my-2 m-auto bg-gray-50 border rounded p-2 md:p-3 flex items-center "
				>
					<img alt="icon" src={link.image} class="w-7 mr-4 ml-14 md:ml-2 md:mr-2 " />
					<div>
						{link.name}
					</div>
				</div>
			</a>
		{/each}
	</div>
</div>
