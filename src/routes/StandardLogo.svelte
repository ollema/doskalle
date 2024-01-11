<script lang="ts">
	const cw = 30; // column width
	const cs = 15; // column spacing
	const cg = 10; // column gap

	export let min_x = 0;
	export let min_y = 0;
	export let width = 4 * cw + 2 * cs + cg;
	export let height = 570; // manual adjustment needed
	export let viewBox = `${min_x} ${min_y} ${width} ${height}`;

	const col_1_x = width / 2 - 2 * cw - cs - cg / 2;
	const col_2_x = width / 2 - cw - cg / 2;
	const col_3_x = width / 2 + cg / 2;
	const col_4_x = width / 2 + cw + cs + cg / 2;

	const letter_fill = '#000000';
	const letter_stroke = '#000000';
	const letter_stroke_width = 0;

	export let filler = false;
</script>

<symbol id="logo-{filler ? 'filler' : 'no-filler'}" {viewBox}>
	<!-- d -->
	<path
		d="M {col_2_x + cw} 0 l {-cw} {cw} v {4 * cw} l -{cw / 2} {-cw / 2} v -{1.5 * cw} l {cw /
			2} -{cw / 2} l -{cw / 2} -{cw / 2} l -{cw} {cw} v {1.5 * cw} l {cw} {cw} l {cw * 1.5} -{cw *
			1.5} z"
		fill={letter_fill}
		stroke={letter_stroke}
		stroke-width={letter_stroke_width}
	/>

	<!-- o -->
	<path
		d="M {col_3_x + cw} {2.5 * cw} l -{cw} {cw} v {0.5 * cw} l {cw} {cw} v -{2.5 * cw} l {cw /
			2} -{cw / 2} l {cw} {cw} v {1.5 * cw} l -{cw} {cw} l -{cw / 2} -{cw / 2} l {cw / 2} -{cw /
			2} v -{1.5 * cw} z"
		fill={letter_fill}
		stroke={letter_stroke}
		stroke-width={letter_stroke_width}
	/>
	<path
		d="M {col_3_x} 0 l {cw} {cw} v {0.37 * cw} h -{cw} z"
		fill={letter_fill}
		stroke={letter_stroke}
		stroke-width={letter_stroke_width}
	/>
	<path
		d="M {col_3_x} {3 * cw} l {cw} {-cw} v -{0.37 * cw} h -{cw} z"
		fill={letter_fill}
		stroke={letter_stroke}
		stroke-width={letter_stroke_width}
	/>

	<!-- s -->
	<path
		d="M {col_1_x} {11 * cw} l {2.5 * cw} -{2.5 * cw} v -{0.5 * cw} l -{cw} -{cw} l -{cw / 2} {cw /
			2} v -{cw} l {cw / 2} -{cw / 2} v {cw} l {cw} -{cw} v -{1.5 * cw} l -{2.5 * cw} {2.5 *
			cw} v {0.5 * cw} l {cw} {cw} l {cw / 2} -{cw / 2} v {cw} l -{cw / 2} {cw /
			2} v {-cw} l -{cw} {cw} z"
		fill={letter_fill}
		stroke={letter_stroke}
		stroke-width={letter_stroke_width}
	/>

	<!-- k -->
	<path
		d="M {col_3_x} {4.5 * cw} v {4 * cw} l {cw} {cw} v -{1 * cw} l {cw / 2} -{cw / 2} v {2 *
			cw} l {cw} {cw} v -{2 * cw} l -{cw} -{cw} l {cw} -{cw} l -{cw} -{cw} l -{cw / 2} {cw /
			2} l {cw / 2} {cw / 2} v {0.5 * cw} l -{cw / 2} {cw / 2} v -{2.5 * cw} z"
		fill={letter_fill}
		stroke={letter_stroke}
		stroke-width={letter_stroke_width}
	/>

	<!-- a -->
	<path
		d="M {col_2_x + cw} {9 * cw} l -{2 * cw + cs} {2 * cw +
			cs} l {cw} {cw} l {cs} -{cs} l -{cs} -{cs} v -{0.5 * cw} l {cs} -{cs} v {2.5 *
			cw} l {cw} {cw} z"
		fill={letter_fill}
		stroke={letter_stroke}
		stroke-width={letter_stroke_width}
	/>

	<!-- l -->
	<path
		d="M {col_3_x} {9 * cw} v {5 * cw} l {cw} -{cw} v -{3 * cw} z"
		fill={letter_fill}
		stroke={letter_stroke}
		stroke-width={letter_stroke_width}
	/>

	<!-- l -->
	<path
		d="M {col_2_x} {13.5 * cw} v {4 * cw} l {cw} -{cw} v -{2 * cw} z"
		fill={letter_fill}
		stroke={letter_stroke}
		stroke-width={letter_stroke_width}
	/>

	<!-- e -->
	<path
		d="M {col_3_x + cw} {13.5 * cw} l -{cw} {cw} v {2 * cw} l {2.5 * cw} {2.5 * cw} v -{3.5 *
			cw} l -{cw} {cw} v {1 * cw} l -{cw / 2} -{cw / 2} v -{cw} l {1.5 * cw} -{1.5 * cw} v -{0.5 *
			cw} l -{1 * cw} -{1 * cw} l -{cw / 2} {cw / 2} l {cw / 2} {cw / 2} v {1 * cw} l -{cw /
			2} {cw / 2} z"
		fill={letter_fill}
		stroke={letter_stroke}
		stroke-width={letter_stroke_width}
	/>

	{#if filler}
		<g>
			<path
				d="M {col_1_x} 0 v {2.5 * cw} l {cw} -{cw} v -{1.5 * cw} z"
				fill={letter_fill}
				stroke={letter_stroke}
				stroke-width={letter_stroke_width}
			/>
			<path
				d="M {col_2_x} 0 v {cs} l {cs} -{cs} z"
				fill={letter_fill}
				stroke={letter_stroke}
				stroke-width={letter_stroke_width}
			/>
			<path
				d="M {col_3_x + cw} 0 v {cs} l -{cs} -{cs} z"
				fill={letter_fill}
				stroke={letter_stroke}
				stroke-width={letter_stroke_width}
			/>
			<path
				d="M {col_4_x} 0 v {1.5 * cw} l {cw} {cw} v -{2.5 * cw} z"
				fill={letter_fill}
				stroke={letter_stroke}
				stroke-width={letter_stroke_width}
			/>
		</g>
	{/if}
</symbol>
