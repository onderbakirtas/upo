<script lang="ts">
	import { slide, fade } from 'svelte/transition';
  import { linear } from 'svelte/easing'

	export let open: boolean = false;
</script>

{#if open}
	<div class="collapse" transition:fade={{ duration: 200, easing: linear }}>
		<div transition:slide={{ duration: 250 }}>
			<slot />
		</div>
	</div>
{/if}

<style lang="scss">
	.collapse {
		display: block;
	}
</style>
