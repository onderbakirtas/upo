<script lang="ts">
	import type { Size, Theme } from './types';

	export let text: string;
	export let size: Size = 'default';
	export let theme: Theme = 'default';
</script>

<button class={`size-${size} is-${theme}`} on:click>{text}</button>

<style lang="scss">
	button {
		display: inline-flex;
		align-items: center;
		user-select: none;
		cursor: pointer;
		border: 1px solid transparent;
		border-radius: 0.25rem;
		font-weight: bold;
		font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell,
			'Open Sans', 'Helvetica Neue', sans-serif;

		&:hover {
			transition: 0.1s;
		}

		&:active {
			transform: translateY(1px);
		}

		&.size {
			&-small {
				height: 28px;
				font-size: 12px;
				line-height: 28px;
				padding: 0 16px;
			}

			&-medium {
				height: 36px;
				font-size: 14px;
				line-height: 36px;
				padding: 0 20px;
			}

			&-default {
				height: 44px;
				font-size: 14px;
				line-height: 44px;
				padding: 0 1.5rem;
			}

			&-large {
				height: 54px;
				font-size: 18px;
				line-height: 54px;
				padding: 0 32px;
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
