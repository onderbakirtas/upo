<script lang="ts">
	import type { Size } from './types';

	export let size: Size = 'default';
</script>

<div class={`input size-${size}`}>
	<input type="text" />
</div>

<style lang="scss">
	.input {
		width: 100%;

		&.size {
			&-tiny {
				height: 26px;
				font-size: 10px;
				line-height: 26px;

				& > input {
					padding: 0 0.5rem;
				}
			}

			&-small {
				height: 30px;
				font-size: 12px;
				line-height: 30px;

				& > input {
					padding: 0 0.625rem;
				}
			}

			&-default {
				height: 36px;
				font-size: 14px;
				line-height: 36px;

				& > input {
					padding: 0 0.75rem;
				}
			}

			&-medium {
				height: 44px;
				font-size: 14px;

				& > input {
					padding: 0 1rem;
				}
			}

			&-large {
				height: 54px;
				font-size: 18px;
				line-height: 54px;

				& > input {
					padding: 0 1.25rem;
				}
			}
		}

		& > input {
			width: 100%;
			height: 100%;
			border-radius: 0.25rem;
			border: 1px solid lightgray;
			outline: none;
			font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell,
				'Open Sans', 'Helvetica Neue', sans-serif;
			font-size: inherit;

			&:focus {
				border-color: royalblue;
			}
		}
	}
</style>
