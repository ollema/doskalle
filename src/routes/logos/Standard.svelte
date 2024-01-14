<script lang="ts">
	import StandardLogo from './StandardLogo.svelte';

	let min_x: number;
	let min_y: number;
	let width: number;
	let height: number;
	let viewBox: string;

	export let filler = false;
</script>

<svg {viewBox} xmlns="http://www.w3.org/2000/svg" {width}>
	<StandardLogo bind:min_x bind:min_y bind:width bind:height bind:viewBox {filler} />

	<use href="#logo-{filler ? 'filler' : 'no-filler'}" x={min_x} y={min_y} {width} {height} />
</svg>
