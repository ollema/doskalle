<script lang="ts">
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
</script>

<div class="w-full text-center text-2xl">without border</div>
<div
	class="grid w-full grid-cols-2 place-items-center gap-8 pt-4 sm:grid-cols-3 md:grid-cols-5 lg:grid-cols-9"
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
	class="grid w-full grid-cols-2 place-items-center gap-8 pt-4 sm:grid-cols-3 md:grid-cols-5 lg:grid-cols-9"
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
