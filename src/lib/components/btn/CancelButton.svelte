<script lang="ts">
</script>

<button
	type="button"
	class="px-2 py-1 border bg-red-400 hover:bg-red-500 rounded-md"
	{...$$restProps}
	on:click>
	<slot />
</button>
