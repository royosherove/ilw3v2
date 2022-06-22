<script>
	import LiveStream from '../components/LiveStream.svelte';
	import LinkTree from '../components/LinkTree.svelte';
	import EventsCalendar from '../components/EventsCalendar.svelte';
	import Notice from '../components/Notice.svelte';
	import Videos from '../components/Videos.svelte';
</script>

<!-- <EventsCalendar/> -->

<div class="m-auto md:w-2/4 flex-col flex text-center space-y-2">
	<a href="/about" class="bg-gray-100 w-40 m-auto rounded text-blue-500 text-center text-xl py-4" >המשימה שלנו</a>
	<Videos max={2}/>
	<LinkTree />
	<EventsCalendar />
	<Notice/>
	<LiveStream />
</div>
