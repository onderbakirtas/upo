<script>
	import Button from '$lib/Button.svelte';
	import Input from '$lib/Input.svelte';
</script>

<h1>Welcome to Upo</h1>

<fieldset>
	<legend>Button Themes</legend>
	<div class="buttons">
		<Button text="Blue" theme="blue" />
		<Button text="Green" theme="green" />
		<Button text="Red" theme="red" />
		<Button text="Orange" theme="orange" />
		<Button text="Default" theme="default" />
	</div>
</fieldset>

<fieldset>
	<legend>Button Sizes</legend>
	<div class="buttons">
		<Button text="Tiny" size="tiny" theme="blue" />
		<Button text="Small" size="small" theme="blue" />
		<Button text="Medium" size="medium" theme="blue" />
		<Button text="Large" size="large" theme="blue" />
		<Button text="Xlarge" size="xlarge" theme="blue" />
	</div>
</fieldset>

<fieldset>
	<legend>Input</legend>
	<div class="inputs">
		<Input size="tiny" />
		<Input size="small" />
		<Input size="medium" />
		<Input size="large" />
		<Input size="xlarge" />
	</div>
</fieldset>

<style lang="scss">
	fieldset {
		padding: 1rem;

		& + & {
			margin-top: 2rem;
		}

		& legend {
			font-family: sans-serif;
			font-size: 16px;
			padding: 0 8px;
			font-weight: bold;
		}

		& > .buttons > :global(* + *) {
			margin-left: 12px;
		}

		& > .inputs > :global(* + *) {
			margin-top: 1rem;
		}
	}
</style>
