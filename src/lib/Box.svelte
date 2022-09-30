<script lang="ts">
	import type { Size } from './types';

	export let spacing: Size = 'medium';
	export let width: string = 'auto';
	export let radius: Size = 'medium';
</script>

<div class="box spacing-{spacing} radius-{radius}" style:width>
	<slot />
</div>

<style lang="scss">
	@import './styles/variables/sizes.scss';

	.box {
		background-color: white;
		border-radius: $radius-small;
		box-shadow: 0 5px 20px lightgray;

		&.radius {
			&-tiny {
				border-radius: $radius-tiny;
			}

			&-small {
				border-radius: $radius-small;
			}

			&-medium {
				border-radius: $radius-medium;
			}

			&-large {
				border-radius: $radius-large;
			}

			&-xlarge {
				border-radius: $radius-xlarge;
			}
		}

		&.spacing {
			&-tiny {
				padding: 10px;
			}

			&-small {
				padding: 15px;
			}

			&-medium {
				padding: 25px;
			}

			&-large {
				padding: 40px;
			}

			&-xlarge {
				padding: 50px;
			}
		}
	}
</style>
