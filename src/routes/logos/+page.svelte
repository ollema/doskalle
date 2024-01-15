<script lang="ts">
	import logo_basic_1 from './logo_basic_1.svg?raw';
	import logo_basic_2 from './logo_basic_2.svg?raw';
	import logo_filled_1 from './logo_filled_1.svg?raw';
	import logo_filled_2 from './logo_filled_2.svg?raw';
	import logo_filled_3 from './logo_filled_3.svg?raw';
	import logo_boxy_1 from './logo_boxy_1.svg?raw';
	import logo_boxy_2 from './logo_boxy_2.svg?raw';
	import logo_boxy_3 from './logo_boxy_3.svg?raw';
	import logo_basic_1_border from './logo_basic_1_border.svg?raw';
	import logo_boxy_1_border from './logo_boxy_1_border.svg?raw';
	import logo_boxy_2_border from './logo_boxy_2_border.svg?raw';
	import logo_boxy_3_border from './logo_boxy_3_border.svg?raw';
</script>

<div class="w-full text-center text-2xl">without border</div>
<div class="flex w-full items-center justify-center gap-8 p-4">
	<div class="flex w-[120px] flex-col items-center gap-4 hover:text-red-700">
		<div class="text-xl">basic 1</div>
		{@html logo_basic_1}
	</div>
	<div class="flex w-[120px] flex-col items-center gap-4 hover:text-red-700">
		<div class="text-xl">basic 2</div>
		{@html logo_basic_2}
	</div>
	<div class="flex w-[120px] flex-col items-center gap-4 hover:text-red-700">
		<div class="text-xl">filled 1</div>
		{@html logo_filled_1}
	</div>
	<div class="flex w-[120px] flex-col items-center gap-4 hover:text-red-700">
		<div class="text-xl">filled 2</div>
		{@html logo_filled_2}
	</div>
	<div class="flex w-[120px] flex-col items-center gap-4 hover:text-red-700">
		<div class="text-xl">filled 3</div>
		{@html logo_filled_3}
	</div>
	<div class="flex w-[120px] flex-col items-center gap-4 hover:text-red-700">
		<div class="text-xl">boxy 1</div>
		{@html logo_boxy_1}
	</div>
	<div class="flex w-[120px] flex-col items-center gap-4 hover:text-red-700">
		<div class="text-xl">boxy 2</div>
		{@html logo_boxy_2}
	</div>
	<div class="flex w-[120px] flex-col items-center gap-4 hover:text-red-700">
		<div class="text-xl">boxy 3</div>
		{@html logo_boxy_3}
	</div>
</div>

<div class="w-full pt-4 text-center text-2xl">with border</div>
<div class="flex w-full items-center justify-center gap-8 p-4">
	<!-- <div class="flex w-[150px] flex-col items-center gap-4 hover:text-red-700">
		<div class="text-xl">basic 1</div>
		{@html logo_basic_1_border}
	</div> -->
	<div class="flex w-[150px] flex-col items-center gap-4 hover:text-red-700">
		<div class="text-xl">boxy 1</div>
		{@html logo_boxy_1_border}
	</div>
	<div class="flex w-[150px] flex-col items-center gap-4 hover:text-red-700">
		<div class="text-xl">boxy 2</div>
		{@html logo_boxy_2_border}
	</div>
	<div class="flex w-[150px] flex-col items-center gap-4 hover:text-red-700">
		<div class="text-xl">boxy 3</div>
		{@html logo_boxy_3_border}
	</div>
</div>
