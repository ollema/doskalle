<script lang="ts">
	import { Slider } from '$lib/components/ui/slider';

	import logo_basic_1 from '$lib/logos/logo_basic_1.svg?raw';
	import logo_basic_2 from '$lib/logos/logo_basic_2.svg?raw';
	import logo_filled_1 from '$lib/logos/logo_filled_1.svg?raw';
	import logo_filled_2 from '$lib/logos/logo_filled_2.svg?raw';
	import logo_filled_3 from '$lib/logos/logo_filled_3.svg?raw';
	import logo_boxy_1 from '$lib/logos/logo_boxy_1.svg?raw';
	import logo_boxy_2 from '$lib/logos/logo_boxy_2.svg?raw';
	import logo_boxy_3 from '$lib/logos/logo_boxy_3.svg?raw';
	import logo_boxy_4 from '$lib/logos/logo_boxy_4.svg?raw';
	import logo_basic_1_border from '$lib/logos/logo_basic_1_border.svg?raw';
	import logo_basic_2_border from '$lib/logos/logo_basic_2_border.svg?raw';
	import logo_filled_1_border from '$lib/logos/logo_filled_1_border.svg?raw';
	import logo_filled_2_border from '$lib/logos/logo_filled_2_border.svg?raw';
	import logo_filled_3_border from '$lib/logos/logo_filled_3_border.svg?raw';
	import logo_boxy_1_border from '$lib/logos/logo_boxy_1_border.svg?raw';
	import logo_boxy_2_border from '$lib/logos/logo_boxy_2_border.svg?raw';
	import logo_boxy_3_border from '$lib/logos/logo_boxy_3_border.svg?raw';
	import logo_boxy_4_border from '$lib/logos/logo_boxy_4_border.svg?raw';

	import { web_storage } from 'svelte-web-storage';

	const noise = web_storage('noise', 30);
	let value = [$noise];
	$: $noise = value[0];
</script>

<svg xmlns="http://www.w3.org/2000/svg" class="absolute h-0 w-0 overflow-hidden">
	<defs>
		<filter id="noisy-distort">
			<feTurbulence
				type="turbulence"
				baseFrequency="0.02"
				numOctaves="3"
				result="turbulence"
				seed="666"
			/>
			<feDisplacementMap
				in2="turbulence"
				in="SourceGraphic"
				scale={(10 * value[0]) / 100}
				xChannelSelector="R"
				yChannelSelector="G"
			/>
		</filter>
	</defs>
</svg>

<div class="mb-4 flex w-full items-center justify-center gap-4">
	<div class="text-xl">noise:</div>
	<Slider bind:value min={0} max={100} step={1} class="w-full max-w-[80px]" />
	<div class="w-4 text-xl">{value}</div>
</div>

<div class="w-full text-center text-2xl">without border</div>
<div
	class="logos grid w-full grid-cols-2 place-items-center gap-8 pt-4 sm:grid-cols-3 md:grid-cols-5 lg:grid-cols-9"
>
	<div
		class="flex w-full max-w-[160px] flex-col items-center justify-center gap-4 hover:text-red-700"
	>
		<div class="text-xl">basic 1</div>
		{@html logo_basic_1}
	</div>
	<div
		class="flex w-full max-w-[160px] flex-col items-center justify-center gap-4 hover:text-red-700"
	>
		<div class="text-xl">basic 2</div>
		{@html logo_basic_2}
	</div>
	<div
		class="flex w-full max-w-[160px] flex-col items-center justify-center gap-4 hover:text-red-700"
	>
		<div class="text-xl">filled 1</div>
		{@html logo_filled_1}
	</div>
	<div
		class="flex w-full max-w-[160px] flex-col items-center justify-center gap-4 hover:text-red-700"
	>
		<div class="text-xl">filled 2</div>
		{@html logo_filled_2}
	</div>
	<div
		class="flex w-full max-w-[160px] flex-col items-center justify-center gap-4 hover:text-red-700"
	>
		<div class="text-xl">filled 3</div>
		{@html logo_filled_3}
	</div>
	<div
		class="flex w-full max-w-[160px] flex-col items-center justify-center gap-4 hover:text-red-700"
	>
		<div class="text-xl">boxy 1</div>
		{@html logo_boxy_1}
	</div>
	<div
		class="flex w-full max-w-[160px] flex-col items-center justify-center gap-4 hover:text-red-700"
	>
		<div class="text-xl">boxy 2</div>
		{@html logo_boxy_2}
	</div>
	<div
		class="flex w-full max-w-[160px] flex-col items-center justify-center gap-4 hover:text-red-700"
	>
		<div class="text-xl">boxy 3</div>
		{@html logo_boxy_3}
	</div>
	<div class="flex w-full max-w-[160px] flex-col items-center gap-4 hover:text-red-700">
		<div class="text-xl">boxy 4</div>
		{@html logo_boxy_4}
	</div>
</div>

<div class="w-full pt-12 text-center text-2xl">with border</div>
<div
	class="logos grid w-full grid-cols-2 place-items-center gap-8 pt-4 sm:grid-cols-3 md:grid-cols-5 lg:grid-cols-9"
>
	<div class="flex w-full max-w-[160px] flex-col items-center gap-4 hover:text-red-700">
		<div class="text-xl">basic 1</div>
		{@html logo_basic_1_border}
	</div>
	<div class="flex w-full max-w-[160px] flex-col items-center gap-4 hover:text-red-700">
		<div class="text-xl">basic 2</div>
		{@html logo_basic_2_border}
	</div>
	<div class="flex w-full max-w-[160px] flex-col items-center gap-4 hover:text-red-700">
		<div class="text-xl">filled 1</div>
		{@html logo_filled_1_border}
	</div>
	<div class="flex w-full max-w-[160px] flex-col items-center gap-4 hover:text-red-700">
		<div class="text-xl">filled 2</div>
		{@html logo_filled_2_border}
	</div>
	<div class="flex w-full max-w-[160px] flex-col items-center gap-4 hover:text-red-700">
		<div class="text-xl">filled 3</div>
		{@html logo_filled_3_border}
	</div>
	<div
		class="flex w-full max-w-[160px] flex-col items-center justify-center gap-4 hover:text-red-700"
	>
		<div class="text-xl">boxy 1</div>
		{@html logo_boxy_1_border}
	</div>
	<div
		class="flex w-full max-w-[160px] flex-col items-center justify-center gap-4 hover:text-red-700"
	>
		<div class="text-xl">boxy 2</div>
		{@html logo_boxy_2_border}
	</div>
	<div
		class="flex w-full max-w-[160px] flex-col items-center justify-center gap-4 hover:text-red-700"
	>
		<div class="text-xl">boxy 3</div>
		{@html logo_boxy_3_border}
	</div>
	<div class="flex w-full max-w-[160px] flex-col items-center gap-4 hover:text-red-700">
		<div class="text-xl">boxy 4</div>
		{@html logo_boxy_4_border}
	</div>
</div>

<style lang="postcss">
	.logos :global(path) {
		filter: url(#noisy-distort);
	}
</style>
