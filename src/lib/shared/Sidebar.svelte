<script>
	import { faChevronLeft, faChevronRight } from '@fortawesome/free-solid-svg-icons';
	import { Fa } from 'svelte-fa';
	import { Button } from 'svelte-ux';

	export let menuItems = [];

	let isCollapsed = true;

	function toggleSidebar() {
		isCollapsed = !isCollapsed;
	}
</script>

<!-- Sidebar container with conditional width and smooth transition for layout changes -->
<div
	class={`drawer-mobile drawer ${isCollapsed ? 'w-20' : 'w-32'} min-h-screen fixed bg-[#f5fffe] z-[1] md:pt-36 flex flex-col text-[#0D494E] shadow-lg transition-all duration-300`}
>
	<!-- Toggle button to expand/collapse sidebar -->
	<div class="mt-12 p-4 md:mt-5">
		<button class="btn btn-circle btn-ghost" onclick={toggleSidebar}>
			<!-- Icon transition with Fa component directly to avoid Button layout shifts -->
			<span class="text-xl transition-transform duration-300">
				<Fa icon={isCollapsed ? faChevronRight : faChevronLeft} />
			</span>
		</button>
	</div>

	<!-- Menu items list with consistent padding and transition -->
	<ul class="menu p-2">
		{#each menuItems as { label, icon, link }}
			<li class="menu-item">
				<a
					href={link}
					class="flex items-center space-x-4 rounded p-3 py-4 transition-colors duration-100 hover:bg-blue-100"
				>
					<!-- Display icon with Fa component -->
					{#if typeof icon === 'object'}
						<Fa {icon} class="text-lg" />
					{:else}
						<span class="text-lg">{icon}</span>
					{/if}
					{#if !isCollapsed}
						<span class="text-md">{label}</span>
					{/if}
				</a>
			</li>
		{/each}
	</ul>
</div>

<style></style>