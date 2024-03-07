<script>
	import { userData } from '../data/user_data';
	let showMenu = false;

	function toggleMenu() {
		showMenu = !showMenu;
	}
</script>

<header
	class="flex items-center justify-between py-6 px-4 mx-8 border-b-[2px] border-neutral-400 border-dotted"
>
	<a aria-label="duggup-logo" href="/"><img alt="logo" src="/assets/logo.svg" /></a>
	<div class="flex items-center gap-12">
		<ul class="hidden md:flex items-center font-[300] justify-evenly gap-12 text-neutral-800">
			<li>
				<a class="flex items-center gap-2" href="/">
					<img alt="home" src="/assets/home.svg" />
					Home
				</a>
			</li>
			<li>
				<a class="flex items-center gap-2" href="/">
					<img alt="home" src="/assets/explore.svg" />
					Explore
				</a>
			</li>
			<li>
				<a class="flex items-center gap-2" href="/">
					<img alt="home" src="/assets/learn.svg" />
					Learn
				</a>
			</li>
		</ul>

		<a
			class="flex items-center gap-2 font-[300] outline outline-[0.5px] px-6 py-2 rounded-lg border-b-4 border-neutral-700"
			href="/"
		>
			<img alt="home" src="/assets/post.svg" />
			Post
		</a>

		<button class="flex items-center gap-3">
			<span class="outline overflow-hidden outline-1 rounded-full outline-neutral-700">
				<img class=" w-10" alt="profile pricture" src={userData.profile_img} />
			</span>
			<p class=" text-neutral-800 font-[450] text-xl">{userData.name}</p>
			<img alt="chevron down" src="/assets/chevron-down.svg" />
		</button>
		<button on:click={toggleMenu} class="block md:hidden" aria-label="dropdown menu">
			<img width="24" alt="menu" src="/assets/hamburger.svg" />
		</button>
		{#if showMenu}
			<div
				class="fixed flex md:hidden justify-center items-center z-[100] top-0 bg-white left-0 w-[100vw] h-[100dvh]"
			>
				<ul class="flex flex-col items-center font-[300] justify-evenly gap-12 text-neutral-800">
					<li>
						<a class="flex items-center gap-2 py-1 border-b-[1px] border-neutral-800" href="/">
							<img alt="home" src="/assets/home.svg" />
							Home
						</a>
					</li>
					<li>
						<a class="flex items-center gap-2 py-1 border-b-[1px] border-neutral-800" href="/">
							<img alt="home" src="/assets/explore.svg" />
							Explore
						</a>
					</li>
					<li>
						<a class="flex items-center gap-2 py-1 border-b-[1px] border-neutral-800" href="/">
							<img alt="home" src="/assets/learn.svg" />
							Learn
						</a>
					</li>
				</ul>
				<button on:click={toggleMenu} class="absolute top-4 right-4 z-[120]">
					<img width="24" alt="close" src="/assets/close.svg" />
				</button>
			</div>
		{/if}
	</div>
</header>
