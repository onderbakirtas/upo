<script lang="ts">
	import { slide, fade } from 'svelte/transition';

	export let open: boolean = false;
</script>

{#if open}
	<div class="collapse " transition:slide={{ duration: 250 }}>
		<slot />
	</div>
{/if}

<style lang="scss">
	.collapse {
		display: block;
	}
</style>
