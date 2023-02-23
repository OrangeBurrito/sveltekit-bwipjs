<script lang="ts">
	import BarcodeLabel from "$lib/components/BarcodeLabel.svelte";

</script>

<p>Barcode!</p>
<h1>some things</h1>
<h2>some other things</h2>
<h2>even more things</h2>

<BarcodeLabel text="ohmygosh"/>
<BarcodeLabel text="whatisthis" labels={['four', 'five', 'six']}/>
<BarcodeLabel text="printacode" labels={['seven', 'eight', 'nine', 'ten']}/>