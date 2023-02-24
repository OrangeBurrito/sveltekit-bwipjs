<script lang="ts">
	import BwipJs from "bwip-js";
	import { onMount } from "svelte";

	let canvas: HTMLCanvasElement

	export let value: string = 'oooooo'

	onMount(() => {
		BwipJs.toCanvas(canvas, {
			bcid: "code128",
			text: value,
			scale: 1
		})
	})
</script>

<canvas bind:this={canvas}></canvas>

<style>
	canvas {
		/* Width and height of the barcode as CSS variables, used as component props */
		width: var(--width);
		height: var(--height);
		display: block;
		image-rendering: crisp-edges;
	}
</style>