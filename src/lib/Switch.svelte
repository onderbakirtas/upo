<script lang="ts">
	import type { Size } from './types';

	const id = Math.floor(Math.random() * Date.now()).toString();

	export let label: string = '';
	export let size: Size = 'medium';
	export let rounded: boolean = false;
</script>

<div class="switch size-{size}" class:rounded>
	<input type="checkbox" name={id} {id} />
	<label for={id}>{label}</label>
</div>

<style lang="scss">
	@import './styles/variables/sizes.scss';

	.switch {
		display: flex;
		align-items: center;
		user-select: none;

		&.rounded > input {
			&::before,
			&::after {
				border-radius: 99px;
			}
		}

		& > * {
			cursor: pointer;
		}

		& > input {
			appearance: none;
			position: relative;
      margin: 0;

			&::before,
			&::after {
				content: '';
				display: block;
				border-radius: 4px;
				transition: 0.15s;
			}

			&::before {
				display: block;
				width: 36px;
				height: 20px;
				background-color: silver;
				position: relative;
				z-index: 1;
			}

			&::after {
				height: 12px;
				width: 12px;
				background-color: white;
				position: absolute;
				left: 4px;
				top: 4px;
				z-index: 2;
			}

			&:checked {
				&::before {
					background-color: royalblue;
				}

				&::after {
					left: 20px;
				}
			}
		}

		& > label {
			padding-left: 8px;
		}
	}
</style>
