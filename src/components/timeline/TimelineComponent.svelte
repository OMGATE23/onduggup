<script>
	import Story from './Story.svelte';
	import JobUpdate from './JobUpdate.svelte';
	import { userData } from '../../data/user_data';
	let timeline = userData.timeline;
</script>

<div class=" w-full flex flex-col items-end md:items-center pr-8">
	{#each timeline as event, index (index)}
		{#if event.type === 'stories'}
			<Story story={event} />
		{/if}
		{#if event.type === 'job_update'}
			<JobUpdate job_update={event} />
		{/if}
	{/each}
</div>
