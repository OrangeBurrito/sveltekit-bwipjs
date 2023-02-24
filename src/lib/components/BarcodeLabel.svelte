<script lang="ts">
	import Barcode from "$lib/components/Barcode.svelte";

	/**
	 *	The text value to be rendered as a barcode.
	 */
	export let value: string = ''
	/**
	 * Text to be displayed above the barcode. Takes in an array of strings.
	 */
	export let text: string[] = ['one', 'two', 'three']
</script>

<barcode-label>
	<barcode-text>
		{#each text as t}
		<span>{t}</span>
		{/each}
	</barcode-text>
	<Barcode {value} --width='var(--barcode-width)' --height='var(--barcode-height)'/>
</barcode-label>

<style>
	barcode-label {
		--barcode-width: 100%;
		--barcode-height: 100px;

		display: inline-block;
		
		font-family: var(--font-mono);
		font-size: 1rem;
	}

	barcode-text {
		display: flex;
		gap: 2ch;
	}

	@media print {
		barcode-label {
			--barcode-width: 80%;
			--barcode-height: 40%;

			height: 100vh;
			width: 100vw;

			display: flex;
			flex-direction: column;
			justify-content: center;
			align-items: center;

			font-size: 5vw; /* use viewport units for responsive font size */
		}
	}
</style>