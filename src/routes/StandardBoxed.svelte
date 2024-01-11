<script lang="ts">
	import StandardLogo from './StandardLogo.svelte';

	let min_x: number;
	let min_y: number;
	let width: number;
	let height: number;
	let viewBox: string;

	const box_offset = 12;
	const box_width = 10;

	$: svgViewBox = `${min_x} ${min_y} ${width + 2 * (box_offset + box_width)} ${
		height + 2 * (box_offset + box_width)
	}`;
	$: svgWidth = width + 2 * (box_offset + box_width);
	$: svgHeigth = height + 2 * (box_offset + box_width);

	export let filler = false;
</script>

<svg viewBox={svgViewBox} xmlns="http://www.w3.org/2000/svg" width={svgWidth} height={svgHeigth}>
	<StandardLogo bind:min_x bind:min_y bind:width bind:height bind:viewBox {filler} />

	<use
		href="#logo-{filler ? 'filler' : 'no-filler'}"
		x={min_x + box_offset + box_width}
		y={min_y + box_offset + box_width}
		{width}
		{height}
	/>

	<!-- box -->
	<rect
		x={min_x + box_width}
		y={min_y + box_width}
		width={svgWidth - 2 * box_width}
		height={svgHeigth - 2 * box_width}
		fill="none"
		stroke="#000000"
		stroke-width={box_width}
	/>
</svg>
