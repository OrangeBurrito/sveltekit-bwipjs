<script lang="ts">
	import BwipJs from "bwip-js";
	import { onMount } from "svelte";

	let canvas: HTMLCanvasElement

	export let text: string = ""
	// width and height are percentages
	export let width: number = 80
	export let height: number = 40

	onMount(() => {
		BwipJs.toCanvas(canvas, {
			bcid: "code128",
			text: text,
			scale: 1
		})
	})
</script>

<canvas bind:this={canvas} style={`width: ${width}%; height: ${height}%`}></canvas>

<style>
	canvas {
		display: block;
		image-rendering: crisp-edges;
	}
</style>