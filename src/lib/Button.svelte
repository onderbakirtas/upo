<script lang="ts">
	type TSize = 'default' | 'small' | 'medium' | 'large';
	type TTheme = 'default' | 'blue' | 'green' | 'red' | 'orange';

	export let text: string;
	export let size: TSize = 'default';
	export let theme: TTheme = 'default';
</script>

<button class={`size-${size} is-${theme}`}>{text}</button>

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

		&.size {
			&-small {
				height: 32px;
				font-size: 12px;
				line-height: 32px;
				padding: 0 16px;
			}

      &-medium {
        height: 36px;
        font-size: 14px;
        line-height: 36px;
        padding: 0 24px;
      }

			&-default {
				height: 2.5rem;
				font-size: 14px;
				line-height: 48px;
				padding: 0 1.5rem;
			}

			&-large {
				height: 64px;
				font-size: 18px;
				line-height: 64px;
				padding: 0 20px;
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
