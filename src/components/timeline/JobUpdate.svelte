<script>
	import { userData } from '../../data/user_data';
	export let job_update = userData.timeline[1];
</script>

<div class="relative w-[50%] mx-auto">
	<div
		class="absolute w-[30%] flex flex-col items-end text-right p-4 px-8 top-[50%] move-up right-[100%]"
	>
		<img class="rounded-full" width="32" alt={job_update.company} src={job_update.company_img} />
		<p class="font-bold">{job_update.company}</p>
		<p class="text-xs text-[#7A9299]">{job_update.location}</p>
		<div class="text-xs text-[#7A9299]">
			Joined <p>{job_update.date}</p>
		</div>
	</div>
	<img
		class="relative move-left top-0 left-0"
		alt="timeline story separator"
		src="/assets/job-update-bar.svg"
	/>
	<div
		style="box-shadow: 0px 1px 2px 0px #DBE5F540;"
		class="min-w-[90%] absolute left-12 top-[50%] move-up bg-white flex flex-col gap-2 py-4 px-5 rounded-lg"
	>
		<p class="text-xl font-[600]">{job_update.title}</p>
		<p class="flex gap-2 text-xs text-[#7A9299]">
			{#each job_update.job_style as job_style, index}
				<p>{job_style}</p>
				{#if index !== job_update.job_style.length - 1}
					<span>•</span>
				{/if}
			{/each}
		</p>
	</div>
</div>
