<script>
	import { userData } from '../../data/user_data';
	export let story = userData.timeline[0];
	let content = story.content;
</script>

<div class="relative w-[50%] mx-auto">
	<div
		class="absolute w-[30%] flex flex-col items-end text-right p-4 px-6 top-[50%] move-up right-[100%]"
	>
		<p class="text-xs text-[#7A9299]"><span>{story.date}</span></p>
	</div>
	<img
		class="relative move-left top-0 left-0"
		alt="timeline story separator"
		src="/assets/stories-bar.svg"
	/>
	<div
		class="min-w-[80%] absolute left-12 top-[50%] move-up flex items-center gap-8 p-2 rounded-lg h-full"
	>
		{#each content as story}
			<div
				class="bg-white w-[50%] outline outline-[0.5px] outline-[#D0D5DD] h-[80%] rounded-lg overflow-hidden"
			>
				<div class="h-[60%] overflow-hidden">
					<img class="object-cover w-full" alt={story.title} src={story.thumbnail} />
				</div>
				<div class="text-sm p-4 font-[300] flex justify-center items-center text-[#141618]">
					<p class="clamp-2-lines">{story.title}</p>
				</div>
			</div>
		{/each}
	</div>
</div>
