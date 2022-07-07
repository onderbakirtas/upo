<script lang="ts">
	import type { Size, Theme } from './types';

	export let text: string;
	export let size: Size = 'medium';
	export let theme: Theme = 'default';
</script>

<button class={`size-${size} is-${theme}`} on:click>{text}</button>

<style lang="scss">
	@import './styles/variables/sizes.scss';

	button {
		display: inline-flex;
		align-items: center;
		user-select: none;
		cursor: pointer;
		border: 1px solid transparent;
		border-radius: 0.25rem;
		font-weight: 600;
		line-height: 1;
		font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell,
			'Open Sans', 'Helvetica Neue', sans-serif;

		&:hover {
			transition: 0.15s;
		}

		&:active {
			transform: translateY(1px);
		}

		&.size {
			&-tiny {
				padding: 0 14px;
				font-size: $text-tiny;
				height: $height-tiny;
			}

			&-small {
				padding: 0 18px;
				font-size: $text-small;
				height: $height-small;
			}

			&-medium {
				padding: 0 22px;
				font-size: $text-medium;
				height: $height-medium;
			}

			&-large {
				padding: 0 26px;
				font-size: $text-large;
				height: $height-large;
			}

			&-xlarge {
				padding: 0 32px;
				font-size: $text-xlarge;
				height: $height-xlarge;
			}
		}

		&:not(.is-default) {
			color: white;
		}

		&.is {
			&-default {
				background-color: transparent;

				&:hover {
					border: 1px solid black;
				}
			}

			&-blue {
				background-color: royalblue;

				&:hover {
					background-color: blue;
				}
			}

			&-green {
				background-color: mediumseagreen;

				&:hover {
					background-color: seagreen;
				}
			}

			&-red {
				background-color: crimson;

				&:hover {
					background-color: firebrick;
				}
			}

			&-orange {
				background-color: tomato;

				&:hover {
					background-color: orangered;
				}
			}
		}
	}
</style>
