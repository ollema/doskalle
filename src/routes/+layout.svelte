<script>
	import '../app.pcss';
	import '@fontsource/unifrakturcook';

	import { ModeWatcher, toggleMode } from 'mode-watcher';

	import { Button } from '$lib/components/ui/button';

	import { Moon, Sun } from 'radix-icons-svelte';
</script>

<ModeWatcher />

<nav class="flex w-full items-center justify-center">
	<ul class="flex items-center gap-8 p-4 text-xl">
		<li class="hover:text-red-700 hover:underline">
			<a href="/logos">all logos</a>
		</li>
		<!-- <li class="hover:text-red-700 hover:underline">
			<a href="/logos/standard">with album art</a>
		</li> -->
		<li class="hover:text-red-700 hover:underline">
			<Button variant={'ghost'} on:click={toggleMode} class="p-0 text-xl hover:bg-inherit">
				<div class="hidden dark:block">
					<Sun class="size-4 hover:text-red-700" />
				</div>
				<div class="block dark:hidden">
					<Moon class="size-4 hover:text-red-700" />
				</div>
			</Button>
		</li>
	</ul>
</nav>

<div class="mx-auto w-full max-w-screen-2xl p-4 2xl:px-0">
	<slot />
</div>
