<script>
	import JobUpdate from './JobUpdate.svelte';
	import Story from './Story.svelte';
	import { userData } from '../../data/user_data';
	let timeline = userData.timeline;
</script>

<div>
	{#each timeline as event}
		{#if event.type === 'stories'}
			<Story story={event} />
		{/if}
		{#if event.type === 'job_update'}
			<JobUpdate job_update={event} />
		{/if}
	{/each}
</div>
