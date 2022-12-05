<script lang="ts">
	export let center: boolean = false
	export let block: boolean = false
</script>

<button
	type="button"
	class="px-4 py-2 border bg-gray-300 hover:bg-gray-400 rounded-md"
	class:mx-auto={center}
	class:block
	{...$$restProps}
	on:click>
	<slot />
</button>
