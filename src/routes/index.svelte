<script>
	import Button from '$lib/Button.svelte';
</script>

<h1>Welcome to Upo</h1>

<fieldset>
	<legend>Buttons</legend>
	<div>
    <Button text="Blue" theme="blue" />
		<Button text="Green" theme="green" />
		<Button text="Red" theme="red" />
		<Button text="Orange" theme="orange" />
		<Button text="Default" theme="default" />
	</div>
</fieldset>

<style lang="scss">
	fieldset {
		padding: 1rem;

    & legend {
      font-family: sans-serif;
      font-size: 16px;
      padding: 0 8px;
      font-weight: bold;
    }

		& > div > :global(* + *) {
			margin-left: 12px;
		}
	}
</style>
