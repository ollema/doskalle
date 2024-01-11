<script lang="ts">
	const min_x = 0;
	const min_y = 0;
	const width = 200;
	const height = 1000;
	const viewBox = `${min_x} ${min_y} ${width} ${height}`;

	const show_background = false;

	const show_grid = false;
	const grid_columns = 40;
	const grid_rows = 100;

	const cw = 30;
	const cg = 15;

	const column_height = 1000;
	const column_internal_spacing = 10;
	const column_opacity = 0.0;

	const col_1_x = width / 2 - 2 * cw - cg - column_internal_spacing / 2;
	const col_2_x = width / 2 - cw - column_internal_spacing / 2;
	const col_3_x = width / 2 + column_internal_spacing / 2;
	const col_4_x = width / 2 + cw + cg + column_internal_spacing / 2;

	const letter_fill = '#000000';
	const letter_stroke = '#000000';
	const letter_stroke_width = 0;
</script>

<svg {viewBox} xmlns="http://www.w3.org/2000/svg">
	{#if show_background}
		<rect x={min_x} y={min_y} {width} {height} fill="#F0F0F0" />
	{/if}
	{#if show_grid}
		{#each Array(grid_columns) as _, i}
			<line
				x1={(i * width) / grid_columns - 0.05}
				y1="0"
				x2={(i * width) / grid_columns - 0.05}
				y2={height}
				stroke="gray"
				stroke-width="0.1"
			/>
		{/each}
		{#each Array(grid_rows) as _, i}
			<line
				x1="0"
				y1={(i * height) / grid_rows - 0.05}
				x2={width}
				y2={(i * height) / grid_rows - 0.05}
				stroke="gray"
				stroke-width="0.1"
			/>
		{/each}
	{/if}

	<rect x={col_1_x} y="0" width={cw} height={column_height} fill="black" opacity={column_opacity} />
	<rect x={col_2_x} y="0" width={cw} height={column_height} fill="black" opacity={column_opacity} />
	<rect x={col_3_x} y="0" width={cw} height={column_height} fill="black" opacity={column_opacity} />
	<rect x={col_4_x} y="0" width={cw} height={column_height} fill="black" opacity={column_opacity} />

	<!-- d -->
	<path
		d="M {col_2_x + cw} {cw} l {-cw} {cw} v {4 * cw} l -{cw / 2} {-cw / 2} v -{1.5 * cw} l {cw /
			2} -{cw / 2} l -{cw / 2} -{cw / 2} l -{cw} {cw} v {1.5 * cw} l {cw} {cw} l {cw * 1.5} -{cw *
			1.5} z"
		fill={letter_fill}
		stroke={letter_stroke}
		stroke-width={letter_stroke_width}
	/>

	<!-- o -->
	<path
		d="M {col_3_x + cw} {3.5 * cw} l -{cw} {cw} v {0.5 * cw} l {cw} {cw} v -{2.5 * cw} l {cw /
			2} -{cw / 2} l {cw} {cw} v {1.5 * cw} l -{cw} {cw} l -{cw / 2} -{cw / 2} l {cw / 2} -{cw /
			2} v -{1.5 * cw} z"
		fill={letter_fill}
		stroke={letter_stroke}
		stroke-width={letter_stroke_width}
	/>
	<path
		d="M {col_3_x} {1 * cw} l {cw} {cw} v {0.37 * cw} h -{cw} z"
		fill={letter_fill}
		stroke={letter_stroke}
		stroke-width={letter_stroke_width}
	/>
	<path
		d="M {col_3_x} {4 * cw} l {cw} {-cw} v -{0.37 * cw} h -{cw} z"
		fill={letter_fill}
		stroke={letter_stroke}
		stroke-width={letter_stroke_width}
	/>

	<!-- s -->
	<path
		d="M {col_1_x} {12 * cw} l {2.5 * cw} -{2.5 * cw} v -{0.5 * cw} l -{cw} -{cw} l -{cw / 2} {cw /
			2} v -{cw} l {cw / 2} -{cw / 2} v {cw} l {cw} -{cw} v -{1.5 * cw} l -{2.5 * cw} {2.5 *
			cw} v {0.5 * cw} l {cw} {cw} l {cw / 2} -{cw / 2} v {cw} l -{cw / 2} {cw /
			2} v {-cw} l -{cw} {cw} z"
		fill={letter_fill}
		stroke={letter_stroke}
		stroke-width={letter_stroke_width}
	/>

	<!-- k -->
	<path
		d="M {col_3_x} {5.5 * cw} v {4 * cw} l {cw} {cw} v -{1 * cw} l {cw / 2} -{cw / 2} v {2 *
			cw} l {cw} {cw} v -{2 * cw} l -{cw} -{cw} l {cw} -{cw} l -{cw} -{cw} l -{cw / 2} {cw /
			2} l {cw / 2} {cw / 2} v {0.5 * cw} l -{cw / 2} {cw / 2} v -{2.5 * cw} z"
		fill={letter_fill}
		stroke={letter_stroke}
		stroke-width={letter_stroke_width}
	/>

	<!-- a -->
	<path
		d="M {col_2_x + cw} {10 * cw} l -{2 * cw + cg} {2 * cw +
			cg} l {cw} {cw} l {cg} -{cg} l -{cg} -{cg} v -{0.5 * cw} l {cg} -{cg} v {2.5 *
			cw} l {cw} {cw} z"
		fill={letter_fill}
		stroke={letter_stroke}
		stroke-width={letter_stroke_width}
	/>

	<!-- l -->
	<path
		d="M {col_3_x} {10 * cw} v {5 * cw} l {cw} -{cw} v -{3 * cw} z"
		fill={letter_fill}
		stroke={letter_stroke}
		stroke-width={letter_stroke_width}
	/>

	<!-- l -->
	<path
		d="M {col_2_x} {14.5 * cw} v {4 * cw} l {cw} -{cw} v -{2 * cw} z"
		fill={letter_fill}
		stroke={letter_stroke}
		stroke-width={letter_stroke_width}
	/>

	<!-- e -->
	<path
		d="M {col_3_x + cw} {14.5 * cw} l -{cw} {cw} v {2 * cw} l {2.5 * cw} {2.5 * cw} v -{3.5 *
			cw} l -{cw} {cw} v {1 * cw} l -{cw / 2} -{cw / 2} v -{cw} l {1.5 * cw} -{1.5 * cw} v -{0.5 *
			cw} l -{1 * cw} -{1 * cw} l -{cw / 2} {cw / 2} l {cw / 2} {cw / 2} v {1 * cw} l -{cw /
			2} {cw / 2} z"
		fill={letter_fill}
		stroke={letter_stroke}
		stroke-width={letter_stroke_width}
	/>
</svg>
