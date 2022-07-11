<script>
	import Box from '$lib/Box.svelte';
	import Button from '$lib/Button.svelte';
	import Collapse from '$lib/Collapse.svelte';
	import Input from '$lib/Input.svelte';
	import Label from '$lib/Label.svelte';
	import Switch from '$lib/Switch.svelte';
	import '$lib/styles/core.scss';
	import Notification from '$lib/Notification.svelte';

	let collapseOpened = false;
</script>

<div class="content">
	<h1>Welcome to Upo</h1>
	<fieldset>
		<legend>Button Themes</legend>
		<div class="buttons">
			<Button text="Blue" theme="blue" />
			<Button text="Green" theme="green" />
			<Button text="Red" theme="red" />
			<Button text="Orange" theme="orange" />
			<Button text="Default" theme="default" />
			<Button text="Disabled" disabled />
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
		<legend>Labels</legend>
		<div class="horizontal">
			<Label title="Your Name" />
			<Label
				title="Your Email"
				size="large"
				description="Please enter your email so we can spam you."
			/>
			<Label
				title="Bank Account"
				description="You need to give money to me, for science!"
				required
			/>
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
						ipsam expedita atque sed tenetur? Lorem ipsum dolor sit amet consectetur adipisicing
						elit. Cumque quos ipsa architecto asperiores accusamus dolorum illo nesciunt, tempore
						dicta libero cupiditate quae suscipit nemo iste at, maxime illum. Modi, quas! Lorem,
						ipsum dolor sit amet consectetur adipisicing elit. Atque fuga quos vitae suscipit quas
						necessitatibus asperiores tempora mollitia. Qui at, neque facilis aspernatur velit
						consequuntur tenetur nulla labore deleniti dolores.
					</p>
				</Collapse>
			</div>
		</div>
	</fieldset>

	<fieldset>
		<legend>Box</legend>
		<div class="horizontal">
			<Box>
				<div>
					Lorem, ipsum dolor sit amet consectetur adipisicing elit. Et nihil inventore similique
					enim tenetur ipsam, placeat debitis temporibus accusantium, minus exercitationem,
					laudantium numquam repellat tempore voluptas eum velit sint ullam? Lorem ipsum dolor, sit
					amet consectetur adipisicing elit. Eveniet suscipit ipsa quod quo provident iste, a soluta
					autem commodi voluptas ex ducimus est unde voluptatibus ad error! Harum, laborum facere!
					Lorem ipsum dolor sit amet consectetur adipisicing elit. Earum animi rem quos. Deserunt,
					possimus dolorem quia quis ratione ad sed voluptatem eligendi totam distinctio accusantium
					corporis magni velit voluptates hic.
				</div>
			</Box>
			<Box spacing="large" width="320px">
				<div>
					Lorem, ipsum dolor sit amet consectetur adipisicing elit. Et nihil inventore similique
					enim tenetur ipsam, placeat debitis temporibus accusantium, minus exercitationem,
					laudantium numquam repellat tempore voluptas eum velit sint ullam? Lorem ipsum dolor, sit
					amet consectetur adipisicing elit. Eveniet suscipit ipsa quod quo provident iste, a soluta
					autem commodi voluptas ex ducimus est unde voluptatibus ad error! Harum, laborum facere!
				</div>
			</Box>
		</div>
	</fieldset>

	<fieldset>
		<legend>Notifications</legend>
		<div class="horizontal">
			<Notification title="You are about to release your soul." />
			<Notification
				title="Error occured!"
				description="There are some issues regarding to your login credentials."
				theme="red"
			/>
		</div>
	</fieldset>
</div>

<style lang="scss">
	.collapse-content {
		margin: 0;
	}

	.content {
		padding: 20px 20px 100px;
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
