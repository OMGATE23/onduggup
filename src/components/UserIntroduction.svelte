<script>
	import { userData } from '../data/user_data';
	console.log(userData);
</script>

<div class="flex w-[80%] mx-auto my-12 gap-16">
	<div class="flex flex-col gap-4 items-center">
		<img
			width="120"
			class="outline outline-[5px] outline-[#EAEFF5] rounded-full"
			alt={userData.name}
			src={userData.profile_img}
		/>
		<p class="text-2xl text-center text-[#4B5C6D] font-[600]">{userData.name}</p>
	</div>
	<div class="flex flex-col gap-8">
		<div class="flex justify-between gap-20">
			<p class="w-[75%] text-[#141618] leading-7 space">{userData.description}</p>
			<div class="flex flex-col items-end">
				<img class="w-10 rounded-full" alt={userData.company} src={userData.company_img} />
				<p class="font-[600]">{userData.company}</p>
				<p class="text-[#7A9299] text-xs">{userData.position}</p>
			</div>
		</div>
		<div class="flex justify-between">
			<button
				class="flex items-center gap-2 outline outline-[0.5px] text-[#4D4D4D] px-5 py-1 rounded-[4px] border-b-4 border-[#4D4D4D]"
				href="/"
			>
				Followed
			</button>
			<div class="flex items-center gap-4">
				<a class="flex items-center gap-2" href="/"
					>My website <img alt="my website" src="/assets/external-link.svg" /></a
				>
				<button aria-label="options"><img alt="options" src="/assets/three-dots.svg" /></button>
			</div>
		</div>
	</div>
</div>
