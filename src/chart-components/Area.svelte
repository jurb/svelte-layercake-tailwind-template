<script>
	import { getContext } from 'svelte';

	const { data, xGet, yGet, xScale, yScale, extents } = getContext('LayerCake');

	$: path = 'M' + $data
		.map(d => {
			return $xGet(d) + ',' + $yGet(d);
		})
		.join('L');

	let area;

	$: {
		const yRange = $yScale.range();
		area = path + (
			'L' + $xScale($extents.x[1]) + ',' + yRange[0] +
			'L' + $xScale($extents.x[0]) + ',' + yRange[0] +
			'Z'
		);
	}
</script>

<path class='path-area' d='{area}'></path>

<style>
	.path-area {
		fill: #ab00d610;
	}
</style>

