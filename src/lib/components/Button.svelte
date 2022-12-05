<script lang="ts">
	export let small: boolean = false
</script>

<button
	class="px-4 py-2 border hover:bg-gray-300"
	{...$$restProps}
	on:click>
	<slot />
</button>
