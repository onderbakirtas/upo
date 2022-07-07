<script lang="ts">
	import type { Size } from './types';

	export let size: Size = 'medium';
	export let placeholder: string = '';
</script>

<div class={`input size-${size}`}>
	<input type="text" {placeholder} />
</div>

<style lang="scss">
	@import './styles/variables/sizes.scss';

	.input {
		width: 100%;

		&.size {
			&-tiny {
				font-size: $text-tiny;
				height: $height-tiny;
				& > input {
					padding: 0 10px;
				}
			}

			&-small {
				font-size: $text-small;
				height: $height-small;
				& > input {
					padding: 0 12px;
				}
			}

			&-medium {
				font-size: $text-medium;
				height: $height-medium;
				& > input {
					padding: 0 14px;
				}
			}

			&-large {
				font-size: $text-large;
				height: $height-large;
				& > input {
					padding: 0 16px;
				}
			}

			&-xlarge {
				font-size: $text-xlarge;
				height: $height-xlarge;
				& > input {
					padding: 0 20px;
				}
			}
		}

		& > input {
      display: block;
			width: 100%;
			height: 100%;
			border-radius: 0.25rem;
			border: 1px solid lightgray;
			outline: none;
			font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell,
				'Open Sans', 'Helvetica Neue', sans-serif;
			font-size: inherit;

			&:hover,
			&:focus,
			&:active {
				transition: 0.15s;
			}

			&:focus {
				border-color: royalblue;
			}
		}
	}
</style>
