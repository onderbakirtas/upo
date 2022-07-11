<script lang="ts">
	import type { Size } from './types';

	export let title: string;
	export let description: string = '';
	export let required: boolean = false;
	export let size: Size = 'medium';
</script>

<div class="label size-{size}">
	<div class="title">
		{title}
		{#if required}
			<span class="required">*</span>
		{/if}
	</div>
	{#if description}
		<div class="description">{description}</div>
	{/if}
</div>

<style lang="scss">
	@import './styles/variables/sizes.scss';
	@import './styles/variables/colors.scss';

	.label {
		display: flex;
		flex-direction: column;
		line-height: 1;
		margin-bottom: 5px;

		&.size {
			&-tiny {
				font-size: 10px;
			}

			&-small {
				font-size: 12px;
			}

			&-medium {
				font-size: 14px;
			}

			&-large {
				font-size: 16px;
			}

			&-xlarge {
				font-size: 20px;
			}
		}

		& .title {
			font-size: 1em;
			font-weight: 600;
		}

		& .description {
			font-size: 0.75em;
			color: $color-dim;
			margin-top: 5px;
		}

		& .required {
			color: $color-red;
		}
	}
</style>
