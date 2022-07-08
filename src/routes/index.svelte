<script>
	import Button from '$lib/Button.svelte';
	import Collapse from '$lib/Collapse.svelte';
	import Input from '$lib/Input.svelte';
	import Switch from '$lib/Switch.svelte';

	let collapseOpened = false;
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
		<Button text="Small" size="small" theme="blue" />
		<Button text="Medium" size="medium" theme="blue" />
		<Button text="Large" size="large" theme="blue" />
	</div>
</fieldset>

<fieldset>
	<legend>Inputs</legend>
	<div class="horizontal">
		<Input size="small" />
		<Input size="medium" />
		<Input size="large" />
	</div>
</fieldset>

<fieldset>
	<legend>Switches</legend>
	<div class="horizontal">
		<Switch label="I like to tap switches" />
		<Switch label="Hooray, another switch to tap" rounded />
	</div>
</fieldset>

<fieldset>
	<legend>Collapse</legend>
	<div class="horizontal">
		<div>
			<Button
				text="Toggle collapse"
				theme="blue"
				on:click={() => (collapseOpened = !collapseOpened)}
			/>
			<Collapse open={collapseOpened}>
				<p class="collapse-content">
					Lorem, ipsum dolor sit amet consectetur adipisicing elit. Quos dolor corrupti aut animi
					cumque, voluptate quasi recusandae accusamus ratione omnis aliquid et? Et ex voluptate
					ipsam expedita atque sed tenetur? Lorem ipsum dolor sit amet consectetur adipisicing elit.
					Cumque quos ipsa architecto asperiores accusamus dolorum illo nesciunt, tempore dicta
					libero cupiditate quae suscipit nemo iste at, maxime illum. Modi, quas! Lorem, ipsum dolor
					sit amet consectetur adipisicing elit. Atque fuga quos vitae suscipit quas necessitatibus
					asperiores tempora mollitia. Qui at, neque facilis aspernatur velit consequuntur tenetur
					nulla labore deleniti dolores.
				</p>
			</Collapse>
		</div>
	</div>
</fieldset>

<style lang="scss">
	:global(*) {
		box-sizing: border-box;
	}

  .collapse-content {
    margin: 0;
  }

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

		& > .horizontal > :global(* + *) {
			margin-top: 1rem;
		}
	}
</style>
