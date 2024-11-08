<script>
	import { faChevronDown } from '@fortawesome/free-solid-svg-icons';
	import { Button, cls } from 'svelte-ux';

	let isMenuOpen = false;

	function openMenu() {
		isMenuOpen = true;
	}

	function closeMenu() {
		isMenuOpen = false;
	}
</script>

<div class="fixed left-0 right-0 top-0 justify-between z-[1] bg-[#f5fffe] text-[#0D494E]">
	<div class="navbar mx-auto max-w-5xl justify-between">
		<div class="">
			<div class="dropdown dropdown-hover">
				<!-- svelte-ignore a11y_no_static_element_interactions -->
				<!-- svelte-ignore a11y_mouse_events_have_key_events -->
				<div
					class="btn m-1 flex-nowrap text-[#0D494E] hover:bg-green-100 bg-transparent"
					onmouseover={openMenu}
					onmouseleave={closeMenu}
				>
					Services
					<Button icon={faChevronDown} class={cls("transition-transform", isMenuOpen ? 'rotate-180' : '')}
					></Button>
				</div>

				<ul class="menu dropdown-content z-[1] w-52 rounded-box bg-base-100 p-2 shadow">
					<li><a class="hover:bg-green-100" href="/">Market Runs</a></li>
					<li><a class="hover:bg-green-100" href="/">Local Snacks</a></li>
				</ul>
			</div>
		</div>
		<div class="">
			<a href="/" class="btn btn-ghost text-xl hover:bg-transparent">Backyard Market</a>
		</div>
		<div class="">
			<div class="form-control">
				<input type="text" placeholder="Search" class="input bg-transparent hover:bg-green-100 input-bordered w-24 md:w-auto" />
			</div>
		</div>
	</div>
</div>
