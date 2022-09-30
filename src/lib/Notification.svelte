<script lang="ts">
	import type { Theme } from './types';

	export let title: string;
	export let description: string = '';
	export let theme: Theme = 'blue';
</script>

<div class="notification">
	<span class="notification-bar is-{theme}" />
	<div class="notification-content">
		<div class="title">{title}</div>
		{#if description}
			<div class="description">{description}</div>
		{/if}
	</div>
</div>

<style lang="scss">
	@import './styles/variables/colors.scss';

	.notification {
		display: flex;
		align-items: center;
		padding: 7.5px;
		border-radius: 5px;
		box-shadow: 0 5px 20px lightgray;
		max-width: 90vh;
		width: 360px;
		min-height: 50px;

		&-bar {
			display: block;
			align-self: stretch;
			flex-shrink: 0;
			border-radius: 5px;
			width: 5px;

			&.is {
				&-blue {
					background-color: $color-blue;
				}
				&-green {
					background-color: $color-green;
				}
				&-green {
					background-color: $color-green;
				}
				&-orange {
					background-color: $color-orange;
				}
				&-red {
					background-color: $color-red;
				}
			}
		}

		&-content {
			margin-left: 15px;
			font-size: 14px;
			padding: 5px 0;

			& > .title {
				font-weight: 500;
			}

			& > .description {
				color: $color-dim;
				margin-top: 5px;
			}
		}
	}
</style>
