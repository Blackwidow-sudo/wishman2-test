<script lang="ts">
	export let id: string
	export let label: string
	export let value: string = ''
	export let placeholder: string = ''
</script>

<label for={id}>{label}</label>
<input
	class="px-3 py-2 border rounded-md leading-tight"
	type="text"
	{id}
	{placeholder}
	bind:value />
