<script lang="ts">
	import Barcode from "$lib/components/Barcode.svelte";

	export let text: string = ''
	export let labels: string[] = ['One', 'Two', 'Three']
</script>

<barcode-label>
	<labels>
		{#each labels as label}
		<span>{label}</span>
		{/each}
	</labels>
	<Barcode {text}/>
</barcode-label>

<style>
	barcode-label {
		display: inline-block;
	}

	labels {
		display: flex;
		gap: 1rem;
	}

	@media print {
		barcode-label {
			height: 100vh;
			width: 100vw;
			display: flex;
			flex-direction: column;
			justify-content: center;
			align-items: center;
			gap: 1rem;
		}

		labels {
			gap: 2rem;
			font-size: 3vw;
		}
	}
</style>