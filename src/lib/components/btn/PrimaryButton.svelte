<script lang="ts">
	export let block: boolean = false
	export let center: boolean = false
</script>

<button
	type="button"
	class="px-2 py-1"
	class:block
	class:mx-auto={center}
	{...$$restProps}
	on:click>
	<slot />
</button>
