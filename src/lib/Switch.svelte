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
	@import './styles/variables/colors.scss';

	.switch {
		display: flex;
		align-items: center;
		user-select: none;

		&.rounded > input {
			&::before,
			&::after {
				border-radius: $radius-xlarge;
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
				border-radius: $radius-small;
				transition: 0.15s;
        box-sizing: border-box;
			}

			&::before {
				display: block;
				width: 35px;
				height: 20px;
				background-color: gainsboro;
				position: relative;
				z-index: 1;
			}

			&::after {
				height: 14px;
				width: 14px;
				background-color: white;
				position: absolute;
        left: 0;
        top: 0;
        transform: translate(3px, 3px);
				z-index: 2;
			}

			&:checked {
				&::before {
					background-color: $color-blue;
				}

				&::after {
          transform: translate(18px, 3px);
				}
			}
		}

		& > label {
			padding-left: 8px;
		}
	}
</style>
