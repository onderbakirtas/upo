<script lang="ts">
	import type { InputType, Size } from './types';

	export let size: Size = 'medium';
	export let placeholder: string = '';
	export let value: string = '';
	export let type: InputType = 'text';

	const handleInput = (e: Event) => {
		value = (e.target as HTMLInputElement).value;
	};
</script>

<div class={`input size-${size}`}>
	<input {type} {placeholder} {value} on:input={handleInput} />
</div>

<style lang="scss">
	@import './styles/variables/colors.scss';
	@import './styles/variables/sizes.scss';

	.input {
		width: 100%;

		&.size {
			&-small {
				font-size: $text-small;
				height: $height-small;
				& > input {
					padding: 0 10px;
				}
			}

			&-medium {
				font-size: $text-medium;
				height: $height-medium;
				& > input {
					padding: 0 15px;
				}
			}

			&-large {
				font-size: $text-large;
				height: $height-large;
				& > input {
					padding: 0 20px;
				}
			}
		}

		& > input {
			display: block;
			width: 100%;
			height: 100%;
			border-radius: $radius-small;
			border: 1px solid $color-gray;
			outline: none;
			font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell,
				'Open Sans', 'Helvetica Neue', sans-serif;
			font-size: inherit;

			&[type='number']::-webkit-outer-spin-button,
			&::-webkit-inner-spin-button {
				appearance: none;
				margin: 0;
			}

			&[type='number'] {
				appearance: none;
			}

			&::-ms-reveal {
				display: none;
			}

			&:hover,
			&:focus,
			&:active {
				transition: 0.15s;
			}

			&:hover {
				border-color: darken($color: $color-gray, $amount: 15);
			}

			&:focus {
				border-color: $color-primary;
			}
		}
	}
</style>
