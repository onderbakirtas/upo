<script lang="ts">
	import type { Size } from './types';

	export let spacing: Size = 'medium';
	export let width: string = 'auto';
</script>

<div class="box spacing-{spacing}" style:width>
	<slot />
</div>

<style lang="scss">
	.box {
		background-color: white;
		border-radius: 4px;
    box-shadow: 0 5px 20px lightgray;

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
