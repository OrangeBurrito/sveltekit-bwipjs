<script lang="ts">
	import Barcode from "$lib/components/Barcode.svelte";

	export let text: string = ''
</script>

<barcode-label>
	<Barcode {text}/>
</barcode-label>

<style>
	barcode-label {
		display: inline-block;
	}

	@media print {
		barcode-label {
			height: 100vh;
			width: 100vw;
			display: flex;
			justify-content: center;
			align-items: center;
		}
	}
</style>