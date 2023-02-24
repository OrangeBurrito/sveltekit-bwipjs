<script lang="ts">
	import BarcodeLabel from "$lib/components/BarcodeLabel.svelte";

</script>

<h1>Barcode!</h1>
<h2>some things</h2>
<h3>some other things</h3>
<h4>even more things</h4>
<p>Enable "Fit to Page Width" in the browser Print Dialog</p>

<BarcodeLabel value="ohmygosh"/>
<BarcodeLabel value="ohmygosh" text={['KITVIN', '123456', 'V30']}/>
<BarcodeLabel value="ohmygosh" text={['four', 'five', 'six']}/>
<BarcodeLabel value="ohmygosh" text={['seven', 'eight', 'nine', 'ten']}/>