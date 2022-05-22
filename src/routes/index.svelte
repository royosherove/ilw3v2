<script>
	import LiveStream from '../components/LiveStream.svelte';
	import LinkTree from '../components/LinkTree.svelte';
	import EventsCalendar from '../components/EventsCalendar.svelte';
import Notice from '../components/Notice.svelte';
</script>

<!-- <EventsCalendar/> -->

<div class="m-auto md:w-2/4 flex-col flex text-center space-y-2">
	<LinkTree />
	<EventsCalendar />
	<Notice/>
	<LiveStream />
</div>
