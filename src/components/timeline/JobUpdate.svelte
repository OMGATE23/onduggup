<script>
	import { userData } from '../../data/user_data';
	export let job_update = userData.timeline[1];
</script>

<div class="relative w-[70%] md:w-[50%]">
	<div
		class="absolute text-xs font-[300] text-[#7A9299] w-[30%] flex flex-col gap-[2px] items-end text-right p-4 md:px-8 top-[50%] move-up right-[100%]"
	>
		<img class="rounded-full" width="32" alt={job_update.company} src={job_update.company_img} />
		<p class="font-bold text-base text-[#141618]">{job_update.company}</p>
		<p class="text-xs font-[300] text-[#7A9299]">{job_update.location}</p>
		<div>Joined</div>
		<p>{job_update.date}</p>
	</div>
	<img
		class="relative move-left top-0 left-0"
		alt="timeline story separator"
		src="/assets/job-update-bar.svg"
	/>
	<div
		style="box-shadow: 0px 1px 2px 0px #DBE5F540;"
		class="min-w-[90%] absolute left-6 md:left-12 top-[50%] move-up bg-white flex flex-col gap-2 py-4 px-5 rounded-lg"
	>
		<p class="text-xl font-[600]">{job_update.title}</p>
		<p class="flex gap-1 text-xs font-[300] text-[#7A9299]">
			{#each job_update.job_style as job_style, index (job_style)}
				<p>{job_style}</p>
				{#if index !== job_update.job_style.length - 1}
					<span class="text-[0.5rem]">•</span>
				{/if}
			{/each}
		</p>
	</div>
</div>
