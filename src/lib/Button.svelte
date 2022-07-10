<script lang="ts">
	import type { Size, Theme } from './types';

	export let text: string;
	export let size: Size = 'medium';
	export let theme: Theme = 'default';
</script>

<button type="button" class={`size-${size} is-${theme}`} on:click>{text}</button>

<style lang="scss">
	@import './styles/variables/sizes.scss';
	@import './styles/variables/colors.scss';

	button {
		display: inline-flex;
		align-items: center;
		user-select: none;
		cursor: pointer;
		border: 1px solid transparent;
		border-radius: $radius-small;
		font-weight: 600;
		line-height: 1;
		font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell,
			'Open Sans', 'Helvetica Neue', sans-serif;

		&:hover {
			transition: 0.15s;
		}

		&:active {
			transform: scale(0.95);
		}

		&.size {
			&-small {
				padding: 0 20px;
				font-size: $text-small;
				height: $height-small;
			}

			&-medium {
				padding: 0 24px;
				font-size: $text-medium;
				height: $height-medium;
			}

			&-large {
				padding: 0 30px;
				font-size: $text-large;
				height: $height-large;
			}
		}

		&:not(.is-default) {
			color: white;
		}

		&.is {
			&-default {
				background-color: $color-gray;

				&:hover {
					background-color: darken($color: $color-gray, $amount: 5);
				}

        &:active {
					background-color: darken($color: $color-gray, $amount: 10);
        }
			}

			&-blue {
				background-color: $color-blue;

				&:hover {
					background-color: darken($color: $color-blue, $amount: 5);
				}

				&:active {
					background-color: darken($color: $color-blue, $amount: 10);
				}
			}

			&-green {
				background-color: $color-green;

				&:hover {
					background-color: darken($color: $color-green, $amount: 5);
				}

				&:active {
					background-color: darken($color: $color-green, $amount: 10);
				}
			}

			&-red {
				background-color: $color-red;

				&:hover {
					background-color: darken($color: $color-red, $amount: 5);
				}

				&:active {
					background-color: darken($color: $color-red, $amount: 10);
				}
			}

			&-orange {
				background-color: $color-orange;

				&:hover {
					background-color: darken($color: $color-orange, $amount: 5);
				}

				&:active {
					background-color: darken($color: $color-orange, $amount: 10);
				}
			}
		}
	}
</style>
