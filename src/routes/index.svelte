<script>
	import LiveStream from '../components/LiveStream.svelte';
	import LinkTree from '../components/LinkTree.svelte';
	import EventsCalendar from '../components/EventsCalendar.svelte';
import Notice from '../components/Notice.svelte';
</script>

<!-- <EventsCalendar/> -->

<div class="m-auto md:w-2/4 flex-col flex text-center space-y-2">
	<img src="bored.png" alt="logo" width="200" height="200" class="rounded-full m-auto " />
	<div class="text-white font-mono">קהילת ווב3 בישראל</div>
	<LinkTree />
	<EventsCalendar />
	<Notice/>
	<LiveStream />
</div>
