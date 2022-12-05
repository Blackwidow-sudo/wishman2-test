<script lang="ts">
	import { fade, type FadeParams } from 'svelte/transition'

	export let inParams: FadeParams = {
		delay: 50,
		duration: 50
	}
	export let outParams: FadeParams = {
		duration: 50
	}
</script>

<div in:fade={inParams} out:fade={outParams}>
	<slot />
</div>
