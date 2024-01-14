<script lang="ts">
	import logo_basic from './logo_basic.svg?raw';
	import Standard from './Standard.svelte';
	import StandardBoxed from './StandardBoxed.svelte';
</script>

<div class="flex gap-8 p-4 items-center">
	<div class="w-[160px]">
		{@html logo_basic}
	</div>
	<div>
		<StandardBoxed />
	</div>
	<div>
		<Standard filler={true} />
	</div>
	<div>
		<StandardBoxed filler={true} />
	</div>
</div>
